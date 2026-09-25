# 🛡️ Bob's Release Pilot

> **AI-powered release safety assistant** — know if your code is safe to ship before you ship it.

Built for the **IBM Bob 2.0 Hackathon 2026** using IBM Bob as the primary development AI assistant.

---

## The Problem

Every engineering team has shipped a release that broke something in production — a removed API endpoint, a missed database migration, a dependency that silently bumped a major version. Traditional CI/CD pipelines catch build failures and failed tests, but they don't answer the harder question:

**"Is this changeset actually safe to release to production?"**

Release safety requires cross-cutting judgment: Are there breaking changes? Are the right things tested? Does this meet our compliance requirements? Who else will be affected?

Bob's Release Pilot answers all of that in seconds.

---

## What It Does

Paste any public GitHub or GitLab repository URL. In seconds, you get:

| Check | What it detects |
|---|---|
| **🔴 Breaking Changes** | Removed exports, API signature changes, major dependency bumps, deleted files, `BREAKING CHANGE` commit markers |
| **🟡 Test Coverage Gaps** | Source files modified with no corresponding test changes, untested API routes, business logic, hooks |
| **🟣 SOC2 / ITIL Compliance** | Secret exposure in diffs, missing changelogs, no rollback plan in migrations, undocumented env vars, vague commit messages |
| **📊 Safety Score (0–100)** | Weighted composite across all dimensions, with `SAFE` / `CAUTION` / `UNSAFE` recommendation |

---

## How It Works

```
User pastes repo URL
        │
        ▼
  POST /api/analyze
        │
        ├─→ GitHub / GitLab API
        │     ├─ Repo metadata
        │     ├─ Last 25 commits
        │     └─ File diff (compare base...head)
        │
        ├─→ Breaking Change Engine
        │     ├─ Commit message pattern scan (BREAKING CHANGE, !feat, remove, migration…)
        │     ├─ Removed file detection
        │     ├─ Removed export detection (TypeScript/JS diff analysis)
        │     └─ Major version bump detection in package.json patches
        │
        ├─→ Test Coverage Engine
        │     ├─ Cross-reference changed source files vs changed test files
        │     ├─ Flag untested API routes, services, hooks, components
        │     └─ Detect zero-test changesets (critical)
        │
        ├─→ Compliance Engine (10 checks)
        │     ├─ SOC2: change docs, secret scan, env documentation, dependency audit
        │     └─ ITIL: release notes, rollback plan, config review, availability
        │
        └─→ Safety Scorer
              ├─ Weighted score: Breaking 35% + Compliance 30% + Coverage 25% + Quality 10%
              └─ Recommendation: SAFE (≥72) / CAUTION (50–71) / UNSAFE (<50 or any critical)
                      │
                      ▼
              sessionStorage → Results Dashboard
```

---

## Tech Stack

| Layer | Technology |
|---|---|
| Framework | [Next.js 14](https://nextjs.org) App Router |
| Language | TypeScript (strict mode) |
| Styling | Tailwind CSS — dark theme, zero external UI library |
| API | GitHub REST API v3 · GitLab REST API v4 |
| Fonts | Geist Sans / Geist Mono (Vercel) |
| Deployment | Vercel (zero-config) |
| AI Assistant | **IBM Bob 2.0** |

---

## How IBM Bob 2.0 Built This

This project was built **entirely with IBM Bob 2.0** as the AI coding assistant — not just for scaffolding, but for the full development lifecycle:

### What Bob did

**1. Architecture design**
Bob designed the full analysis pipeline from scratch — identifying the right separation between the repo-fetching layer, the four analysis engines, and the scoring module. The `src/lib/` structure and the data flow from API route → sessionStorage → results page was Bob's design.

**2. Analysis engines**
All four analysis engines (`breaking-changes.ts`, `test-coverage.ts`, `compliance.ts`, `scorer.ts`) were written by Bob — including the regex pattern library for detecting breaking changes in commit messages and diffs, the SOC2/ITIL rule definitions, and the weighted scoring formula.

**3. GitHub & GitLab API integration**
Bob wrote the full `repo-fetcher.ts` abstraction handling both providers — including the 3-dot compare syntax for GitHub diffs, the `owner%2Frepo` URL encoding for GitLab project IDs, and the commit-based fallback for diff base detection.

**4. TypeScript type system**
Bob designed all shared types in `src/types/analysis.ts` and enforced them across the codebase — catching implicit `any[]` issues and `Set` iteration incompatibilities at build time.

**5. Dashboard UI**
The entire dark-theme Tailwind UI — the SVG circular gauge, tabbed results layout, severity-coded panels, compliance check groups, and commit diff viewer — was built by Bob in a single session.

**6. Build validation**
Bob ran `npm run build` iteratively, diagnosed TypeScript errors, and fixed them without human intervention — delivering a clean production build.

### Developer workflow with Bob

```
Human:  "Build a complete release safety assistant with these pages..."
Bob:    → Designed architecture
        → Wrote 21 source files
        → Fixed 3 TypeScript compile errors
        → Produced clean production build
        → Wrote this README
```

Total human lines of code written: **0**. Total files written by Bob: **21**.

---

## Screenshots

> 📸 *Screenshots coming soon — run locally to see the full UI*

**Home Page** — clean URL input with advanced branch/token options
```
[ https://github.com/owner/repo          ] [Analyze Release Safety →]
```

**Results Dashboard** — tabbed view with score gauge and detailed findings
```
┌─────────────────────────────────────────────────────────┐
│  owner/repo          Score: 68/100    ⚠ CAUTION         │
│  ┌──────┐  Breaking: 3   Test Gaps: 2   Compliance: 7   │
│  │  68  │                                                │
│  └──────┘  [Overview] [Breaking·3] [Test Gaps·2] [...]  │
└─────────────────────────────────────────────────────────┘
```

---

## Running Locally

```bash
# 1. Clone the repo
git clone https://github.com/your-username/bobs-release-pilot
cd bobs-release-pilot

# 2. Install dependencies
npm install

# 3. Start the dev server
npm run dev
```

Open [http://localhost:3000](http://localhost:3000).

No environment variables required — the app works against public GitHub/GitLab repos without a token (subject to rate limits: 60 requests/hour unauthenticated).

**Optional — increase API rate limits:**
Add a GitHub personal access token in the Advanced Options panel on the home page. It stays in your browser and is never sent to any server other than the GitHub/GitLab API directly.

### Other commands

```bash
npm run build   # production build
npm run lint    # ESLint check
npm run start   # start production server (after build)
```

---

## Project Structure

```
src/
├── types/
│   └── analysis.ts          # All shared TypeScript interfaces
├── lib/
│   ├── repo-fetcher.ts      # GitHub + GitLab API abstraction
│   ├── breaking-changes.ts  # Breaking change detection engine
│   ├── test-coverage.ts     # Test coverage gap analysis
│   ├── compliance.ts        # SOC2/ITIL compliance rule engine (10 checks)
│   └── scorer.ts            # Safety score + recommendation logic
├── app/
│   ├── page.tsx             # Home page
│   ├── results/page.tsx     # Results dashboard
│   └── api/analyze/
│       └── route.ts         # POST /api/analyze
└── components/
    ├── AnalyzeForm.tsx       # URL input form
    ├── ScoreGauge.tsx        # SVG circular gauge
    ├── BreakingChangePanel.tsx
    ├── TestCoveragePanel.tsx
    ├── CompliancePanel.tsx
    └── CommitList.tsx
```

---

## Scoring Methodology

| Dimension | Weight | How it's calculated |
|---|---|---|
| Breaking Changes | 35% | Penalty per severity: critical −25, high −15, medium −8, low −3 |
| SOC2/ITIL Compliance | 30% | pass=100pts, warning=60pts, fail=0pts, averaged across active checks |
| Test Coverage | 25% | Penalty for untested changed files and critical-area gaps |
| Commit Quality | 10% | Ratio of commits to files; penalizes vague single-word messages |

**Recommendation thresholds:**
- `SAFE` — score ≥ 72, no critical breaking changes
- `CAUTION` — score 50–71
- `UNSAFE` — score < 50, or any critical-severity breaking change

---

## Limitations

- Analysis is **heuristic and static** — it pattern-matches diffs and commit messages, it does not execute code or run tests
- Works on **public repositories** without authentication; private repos require a token with `repo` scope
- GitHub API rate limit: 60 req/hr unauthenticated, 5,000 req/hr with token
- Diff analysis is limited to the most recent ~25 commits and the files changed between oldest and newest fetched commit

---

## License

MIT — built for the IBM Bob 2.0 Hackathon 2026.

---

<div align="center">
  <strong>Built with IBM Bob 2.0</strong> · IBM Bob Hackathon 2026
</div>
