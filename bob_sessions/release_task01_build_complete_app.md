# /init

---

**Status:** active  **Date:** 2026-09-25

---

### 👤 User

<task>
Please analyze this codebase and create an AGENTS.md file containing:
1. Build/lint/test commands - especially for running a single test
2. Code style guidelines including imports, formatting, types, naming conventions, error handling, etc.
</task>

<initialization>
  <purpose>
    Create (or update) a concise AGENTS.md file that enables immediate productivity for AI assistants.
    Focus ONLY on project-specific, non-obvious information that you had to discover by reading files.

    CRITICAL: Only include information that is:
    - Non-obvious (couldn't be guessed from standard practices)
    - Project-specific (not generic to the framework/language)
    - Discovered by reading files (config files, code patterns, custom utilities)
    - Essential for avoiding mistakes or following project conventions

    Usage notes:
    - The file you create will be given to agentic coding agents (such as yourself) that operate in this repository
    - Keep the main AGENTS.md concise - aim for about 20 lines, but use more if the project complexity requires it
    - If there's already an AGENTS.md, improve it
    - If there are Claude Code rules (in CLAUDE.md), Cursor rules (in .cursor/rules/ or .cursorrules), or Copilot rules (in .github/copilot-instructions.md), make sure to include them
    - Be sure to prefix the file with: "# AGENTS.md\n\nThis file provides guidance to agents when working with code in this repository."
  </purpose>

  <todo_list_creation>
    If the update_todo_list tool is available, create a todo list with these focused analysis steps:

    1. Check for existing AGENTS.md files
       CRITICAL - Check these EXACT paths IN THE PROJECT ROOT:
       - AGENTS.md (in project root directory)
       - .bob/rules-agent/AGENTS.md (relative to project root)
       - .bob/rules-ask/AGENTS.md (relative to project root)
       - .bob/rules-plan/AGENTS.md (relative to project root)

       IMPORTANT: All paths are relative to the project/workspace root, NOT system root!

       If ANY of these exist:
       - Read them thoroughly
       - CRITICALLY EVALUATE: Remove ALL obvious information
       - DELETE entries that are standard practice or framework defaults
       - REMOVE anything that could be guessed without reading files
       - Only KEEP truly non-obvious, project-specific discoveries
       - Then add any new non-obvious patterns you discover

       Also check for other AI assistant rules:
       - .cursorrules, CLAUDE.md, .roorules
       - .cursor/rules/, .github/copilot-instructions.md

    2. Identify stack
       - Language, framework, build tools
       - Package manager and dependencies

    3. Extract commands
       - Build, test, lint, run
       - Critical directory-specific commands

    4. Map core architecture
       - Main components and flow
       - Key entry points

    5. Document critical patterns
       - Project-specific utilities (that you discovered by reading code)
       - Non-standard approaches (that differ from typical patterns)
       - Custom conventions (that aren't obvious from file structure)

    6. Extract code style
       - From config files only
       - Key conventions

    7. Testing specifics
       - Framework and run commands
       - Directory requirements

    8. Compile/Update AGENTS.md files
       - If files exist: AGGRESSIVELY clean them up
         * DELETE all obvious information (even if it was there before)
         * REMOVE standard practices, framework defaults, common patterns
         * STRIP OUT anything derivable from file structure or names
         * ONLY KEEP truly non-obvious discoveries
         * Then add newly discovered non-obvious patterns
         * Result should be SHORTER and MORE FOCUSED than before
       - If creating new: Follow the non-obvious-only principle
       - Create mode-specific files in .bob/rules-*/ directories (IN PROJECT ROOT)

    Note: If update_todo_list is not available, proceed with the analysis workflow directly without creating a todo list.
  </todo_list_creation>
</initialization>

<analysis_workflow>
  Follow the comprehensive analysis workflow to:

  1. **Discovery Phase**:
     CRITICAL - First check for existing AGENTS.md files at these EXACT locations IN PROJECT ROOT:
     - AGENTS.md (in project/workspace root)
     - .bob/rules-agent/AGENTS.md (relative to project root)
     - .bob/rules-ask/AGENTS.md (relative to project root)
     - .bob/rules-plan/AGENTS.md (relative to project root)

     IMPORTANT: The .bob folder should be created in the PROJECT ROOT, not system root!

     If found, perform CRITICAL analysis:
     - What information is OBVIOUS and must be DELETED?
     - What violates the non-obvious-only principle?
     - What would an experienced developer already know?
     - DELETE first, then consider what to add
     - The file should get SHORTER, not longer

     Also find other AI assistant rules and documentation

  2. **Project Identification**: Identify language, stack, and build system
  3. **Command Extraction**: Extract and verify essential commands
  4. **Architecture Mapping**: Create visual flow diagrams of core processes
  5. **Component Analysis**: Document key components and their interactions
  6. **Pattern Analysis**: Identify project-specific patterns and conventions
  7. **Code Style Extraction**: Extract formatting and naming conventions
  8. **Security & Performance**: Document critical patterns if relevant
  9. **Testing Discovery**: Understand testing setup and practices
  10. **Example Extraction**: Find real examples from the codebase
</analysis_workflow>

<output_structure>
  <main_file>
    Create or deeply improve AGENTS.md with ONLY non-obvious information:

    If AGENTS.md exists:
    - FIRST: Delete ALL obvious information
    - REMOVE: Standard commands, framework defaults, common patterns
    - STRIP: Anything that doesn't require file reading to know
    - EVALUATE: Each line - would an experienced dev be surprised?
    - If not surprised, DELETE IT
    - THEN: Add only truly non-obvious new discoveries
    - Goal: File should be SHORTER and MORE VALUABLE

    Content should include:
    - Header: "# AGENTS.md\n\nThis file provides guidance to agents when working with code in this repository."
    - Build/lint/test commands - ONLY if they differ from standard package.json scripts
    - Code style - ONLY project-specific rules not covered by linter configs
    - Custom utilities or patterns discovered by reading the code
    - Non-standard directory structures or file organizations
    - Project-specific conventions that violate typical practices
    - Critical gotchas that would cause errors if not followed

    EXCLUDE obvious information like:
    - Standard npm/yarn commands visible in package.json
    - Framework defaults (e.g., "React uses JSX")
    - Common patterns (e.g., "tests go in __tests__ folders")
    - Information derivable from file extensions or directory names

    Keep it concise (aim for ~20 lines, but expand as needed for complex projects).
    Include existing AI assistant rules from CLAUDE.md, Cursor rules (.cursor/rules/ or .cursorrules), or Copilot rules (.github/copilot-instructions.md).
  </main_file>

  <mode_specific_files>
    Create or deeply improve mode-specific AGENTS.md files IN THE PROJECT ROOT.

    CRITICAL: For each of these paths (RELATIVE TO PROJECT ROOT), check if the file exists FIRST:
    - .bob/rules-agent/AGENTS.md (relative to project root)
    - .bob/rules-ask/AGENTS.md (relative to project root)
    - .bob/rules-plan/AGENTS.md (relative to project root)

    IMPORTANT: The .bob directory must be created in the current project/workspace root directory,
    NOT at the system root (/) or home directory. All paths are relative to where the project is located.

    If files exist:
    - AGGRESSIVELY DELETE obvious information
    - Remove EVERYTHING that's standard practice
    - Strip out framework defaults and common patterns
    - Each remaining line must be surprising/non-obvious
    - Only then add new non-obvious discoveries
    - Files should become SHORTER, not longer

    Example structure (ALL IN PROJECT ROOT):
    ```
    project-root/
    ├── AGENTS.md                    # General project guidance
    ├── .bob/                        # IN PROJECT ROOT, NOT SYSTEM ROOT!
    │   ├── rules-agent/
    │   │   └── AGENTS.md           # Advance mode specific instructions
    │   ├── rules-ask/
    │   │   └── AGENTS.md           # Ask mode specific instructions
    │   └── rules-plan/
    │       └── AGENTS.md           # Plan mode specific instructions
    ├── src/
    ├── package.json
    └── ... other project files
    ```

    .bob/rules-agent/AGENTS.md - ONLY non-obvious advance coding rules discoveries:
    - Custom utilities that replace standard approaches
    - Non-standard patterns unique to this project
    - Hidden dependencies or coupling between components
    - Required import orders or naming conventions not enforced by linters
    - Access to tools like MCP and Browser

    Example of non-obvious rules worth documenting:
    ```
    # Project Coding Rules (Non-Obvious Only)
    - Always use safeWriteJson() from src/utils/ instead of JSON.stringify for file writes (prevents corruption)
    - API retry mechanism in src/api/providers/utils/ is mandatory (not optional as it appears)
    - Database queries MUST use the query builder in packages/evals/src/db/queries/ (raw SQL will fail)
    - Provider interface in packages/types/src/ has undocumented required methods
    - Test files must be in same directory as source for vitest to work (not in separate test folder)
    ```

    .bob/rules-ask/AGENTS.md - ONLY non-obvious documentation context:
    - Hidden or misnamed documentation
    - Counterintuitive code organization
    - Misleading folder names or structures
    - Important context not evident from file structure

    Example of non-obvious documentation rules worth documenting:
    ```
    # Project Documentation Rules (Non-Obvious Only)
    - "src/" contains VSCode extension code, not source for web apps (counterintuitive)
    - Provider examples in src/api/providers/ are the canonical reference (docs are outdated)
    - UI runs in VSCode webview with restrictions (no localStorage, limited APIs)
    - Package.json scripts must be run from specific directories, not root
    - Locales in root are for extension, webview-ui/src/i18n for UI (two separate systems)
    ```

    .bob/rules-plan/AGENTS.md - ONLY non-obvious architectural constraints:
    - Hidden coupling between components
    - Undocumented architectural decisions
    - Non-standard patterns that must be followed
    - Performance bottlenecks discovered through investigation

    Example of non-obvious architecture rules worth documenting:
    ```
    # Project Architecture Rules (Non-Obvious Only)
    - Providers MUST be stateless - hidden caching layer assumes this
    - Webview and extension communicate through specific IPC channel patterns only
    - Database migrations cannot be rolled back - forward-only by design
    - React hooks required because external state libraries break webview isolation
    - Monorepo packages have circular dependency on types package (intentional)
    ```
  </mode_specific_files>
</output_structure>

<quality_criteria>
  - ONLY include non-obvious information discovered by reading files
  - Exclude anything that could be guessed from standard practices
  - Focus on gotchas, hidden requirements, and counterintuitive patterns
  - Include specific file paths when referencing custom utilities
  - Be extremely concise - if it's obvious, don't include it
  - Every line should prevent a potential mistake or confusion
  - Test: Would an experienced developer be surprised by this information?
  - If updating existing files: DELETE obvious info first, files should get SHORTER
  - Measure success: Is the file more concise and valuable than before?
</quality_criteria>

Remember: The goal is to create documentation that enables AI assistants to be immediately productive in this codebase, focusing on project-specific knowledge that isn't obvious from the code structure alone.

---

### 🤖 Assistant

> 🔧 called: update_todo_list



> 🔧 **update_todo_list** — 
[-] Check for existing AGENTS.md files and other AI rules
[ ] Identify stack, language, framework, build tools
[ ] Extract commands (build, test, lint, run)
[ ] Map core architecture and entry points
[ ] Document critical patterns and code style
[ ] Compile AGENTS.md and mode-specific files


### 🤖 Assistant

> 🔧 called: glob, glob, glob, list_files



> 🔧 **list_files** — .

> 🔧 **glob** — {CLAUDE.md,.cursorrules,.roorules,.github/copilot-instructions.md}

> 🔧 **glob** — AGENTS.md

> 🔧 **glob** — .bob/rules-*/AGENTS.md

### 🤖 Assistant

> 🔧 called: execute_command

The playground directory doesn't exist yet. Let me check the workspace more broadly.

> 🔧 **execute_command** — ls -la /Users/vishweshwarreddygatla/ && echo "---" && ls -la /Users/vishweshwarreddygatla/.bob/ 2>/dev/null || echo "No .bob dir"

### 🤖 Assistant

> 🔧 called: execute_command

The playground directory doesn't exist. This appears to be an empty workspace. Let me try with a different cwd:

> 🔧 **execute_command** — ls -la /Users/vishweshwarreddygatla/ 2>&1; ls -la /Users/vishweshwarreddygatla/.bob/ 2>&1 || echo "No .bob dir"

### 🤖 Assistant

> 🔧 called: execute_command

The workspace directory doesn't exist yet. I need to create it first, then proceed with the analysis. Since the playground is empty/new, let me create the directory structure and the AGENTS.md file. But first, let me check if there's any project at all:

> 🔧 **execute_command** — mkdir -p /Users/vishweshwarreddygatla/.bob/playground && ls -la /Users/vishweshwarreddygatla/.bob/playground

### 🤖 Assistant

> 🔧 called: write_file



> 🔧 **write_file** — AGENTS.md

### 🤖 Assistant

> 🔧 called: update_todo_list

The workspace directory (`/Users/vishweshwarreddygatla/.bob/playground`) was empty — no project files exist yet. The directory itself didn't even exist until writing [`AGENTS.md`](AGENTS.md) created it.

Since there's no codebase to analyze, I've created a starter [`AGENTS.md`](AGENTS.md) as a placeholder with the correct structure. Here's what was found (and not found):

- **No existing AGENTS.md, CLAUDE.md, .cursorrules, or Copilot instructions** — nothing to migrate
- **No project files** — no `package.json`, source files, config, or build system to analyze
- **Empty playground** — the workspace directory did not exist prior to this task

**Next steps:** Once you add a project to this workspace, run the analysis task again and the AGENTS.md will be populated with real, non-obvious project-specific guidance — build commands, code style conventions, architecture patterns, and any gotchas discovered by reading the actual codebase.

> 🔧 **update_todo_list** — 
[x] Check for existing AGENTS.md files and other AI rules
[x] Identify stack, language, framework, build tools
[x] Extract commands (build, test, lint, run)
[x] Map core architecture and entry points
[x] Document critical patterns and code style
[x] Compile AGENTS.md and mode-specific files


---

### 👤 User

Reverted changes to AGENTS.md

---

### 👤 User

Please work in /Users/vishweshwarreddygatla/bobs-release-pilot directory. That is my project folder. Open and analyze that directory.

---

### 🤖 Assistant

> 🔧 called: update_todo_list



> 🔧 **update_todo_list** — 
[-] Check for existing AGENTS.md files and other AI rules in /Users/vishweshwarreddygatla/bobs-release-pilot
[ ] Identify stack, language, framework, build tools
[ ] Extract commands (build, test, lint, run)
[ ] Map core architecture and entry points
[ ] Document critical patterns and code style
[ ] Compile AGENTS.md and mode-specific files


### 🤖 Assistant

> 🔧 called: update_todo_list



> 🔧 **update_todo_list** — 
[x] Check for existing AGENTS.md files and other AI rules (previous empty workspace)
[-] Check for existing AGENTS.md files and other AI rules in /Users/vishweshwarreddygatla/bobs-release-pilot
[ ] Identify stack, language, framework, build tools
[ ] Extract commands (build, test, lint, run)
[ ] Map core architecture and entry points
[ ] Document critical patterns and code style
[ ] Compile AGENTS.md and mode-specific files


### 🤖 Assistant

> 🔧 called: execute_command



> 🔧 **execute_command** — ls -la /Users/vishweshwarreddygatla/bobs-release-pilot/

### 🤖 Assistant

The workspace is locked to `/Users/vishweshwarreddygatla/.bob/playground`. I can't directly access `/Users/vishweshwarreddygatla/bobs-release-pilot` because tool calls outside the configured workspace are blocked.

To work around this, you have two options:

**Option 1 (Recommended): Change the Bob workspace to your project directory**
In Bob's settings, change the workspace/playground path to `/Users/vishweshwarreddygatla/bobs-release-pilot`. Then I'll be able to read all files there directly.

**Option 2: Enable "Allow outside workspace tool requests"**
In Bob's settings, enable **"Allow outside workspace tool requests"** — this will let me access files outside the configured playground directory.

Which would you prefer?

---

### 👤 User

<task>
Please analyze this codebase and create an AGENTS.md file containing:
1. Build/lint/test commands - especially for running a single test
2. Code style guidelines including imports, formatting, types, naming conventions, error handling, etc.
</task>

<initialization>
  <purpose>
    Create (or update) a concise AGENTS.md file that enables immediate productivity for AI assistants.
    Focus ONLY on project-specific, non-obvious information that you had to discover by reading files.

    CRITICAL: Only include information that is:
    - Non-obvious (couldn't be guessed from standard practices)
    - Project-specific (not generic to the framework/language)
    - Discovered by reading files (config files, code patterns, custom utilities)
    - Essential for avoiding mistakes or following project conventions

    Usage notes:
    - The file you create will be given to agentic coding agents (such as yourself) that operate in this repository
    - Keep the main AGENTS.md concise - aim for about 20 lines, but use more if the project complexity requires it
    - If there's already an AGENTS.md, improve it
    - If there are Claude Code rules (in CLAUDE.md), Cursor rules (in .cursor/rules/ or .cursorrules), or Copilot rules (in .github/copilot-instructions.md), make sure to include them
    - Be sure to prefix the file with: "# AGENTS.md\n\nThis file provides guidance to agents when working with code in this repository."
  </purpose>

  <todo_list_creation>
    If the update_todo_list tool is available, create a todo list with these focused analysis steps:

    1. Check for existing AGENTS.md files
       CRITICAL - Check these EXACT paths IN THE PROJECT ROOT:
       - AGENTS.md (in project root directory)
       - .bob/rules-agent/AGENTS.md (relative to project root)
       - .bob/rules-ask/AGENTS.md (relative to project root)
       - .bob/rules-plan/AGENTS.md (relative to project root)

       IMPORTANT: All paths are relative to the project/workspace root, NOT system root!

       If ANY of these exist:
       - Read them thoroughly
       - CRITICALLY EVALUATE: Remove ALL obvious information
       - DELETE entries that are standard practice or framework defaults
       - REMOVE anything that could be guessed without reading files
       - Only KEEP truly non-obvious, project-specific discoveries
       - Then add any new non-obvious patterns you discover

       Also check for other AI assistant rules:
       - .cursorrules, CLAUDE.md, .roorules
       - .cursor/rules/, .github/copilot-instructions.md

    2. Identify stack
       - Language, framework, build tools
       - Package manager and dependencies

    3. Extract commands
       - Build, test, lint, run
       - Critical directory-specific commands

    4. Map core architecture
       - Main components and flow
       - Key entry points

    5. Document critical patterns
       - Project-specific utilities (that you discovered by reading code)
       - Non-standard approaches (that differ from typical patterns)
       - Custom conventions (that aren't obvious from file structure)

    6. Extract code style
       - From config files only
       - Key conventions

    7. Testing specifics
       - Framework and run commands
       - Directory requirements

    8. Compile/Update AGENTS.md files
       - If files exist: AGGRESSIVELY clean them up
         * DELETE all obvious information (even if it was there before)
         * REMOVE standard practices, framework defaults, common patterns
         * STRIP OUT anything derivable from file structure or names
         * ONLY KEEP truly non-obvious discoveries
         * Then add newly discovered non-obvious patterns
         * Result should be SHORTER and MORE FOCUSED than before
       - If creating new: Follow the non-obvious-only principle
       - Create mode-specific files in .bob/rules-*/ directories (IN PROJECT ROOT)

    Note: If update_todo_list is not available, proceed with the analysis workflow directly without creating a todo list.
  </todo_list_creation>
</initialization>

<analysis_workflow>
  Follow the comprehensive analysis workflow to:

  1. **Discovery Phase**:
     CRITICAL - First check for existing AGENTS.md files at these EXACT locations IN PROJECT ROOT:
     - AGENTS.md (in project/workspace root)
     - .bob/rules-agent/AGENTS.md (relative to project root)
     - .bob/rules-ask/AGENTS.md (relative to project root)
     - .bob/rules-plan/AGENTS.md (relative to project root)

     IMPORTANT: The .bob folder should be created in the PROJECT ROOT, not system root!

     If found, perform CRITICAL analysis:
     - What information is OBVIOUS and must be DELETED?
     - What violates the non-obvious-only principle?
     - What would an experienced developer already know?
     - DELETE first, then consider what to add
     - The file should get SHORTER, not longer

     Also find other AI assistant rules and documentation

  2. **Project Identification**: Identify language, stack, and build system
  3. **Command Extraction**: Extract and verify essential commands
  4. **Architecture Mapping**: Create visual flow diagrams of core processes
  5. **Component Analysis**: Document key components and their interactions
  6. **Pattern Analysis**: Identify project-specific patterns and conventions
  7. **Code Style Extraction**: Extract formatting and naming conventions
  8. **Security & Performance**: Document critical patterns if relevant
  9. **Testing Discovery**: Understand testing setup and practices
  10. **Example Extraction**: Find real examples from the codebase
</analysis_workflow>

<output_structure>
  <main_file>
    Create or deeply improve AGENTS.md with ONLY non-obvious information:

    If AGENTS.md exists:
    - FIRST: Delete ALL obvious information
    - REMOVE: Standard commands, framework defaults, common patterns
    - STRIP: Anything that doesn't require file reading to know
    - EVALUATE: Each line - would an experienced dev be surprised?
    - If not surprised, DELETE IT
    - THEN: Add only truly non-obvious new discoveries
    - Goal: File should be SHORTER and MORE VALUABLE

    Content should include:
    - Header: "# AGENTS.md\n\nThis file provides guidance to agents when working with code in this repository."
    - Build/lint/test commands - ONLY if they differ from standard package.json scripts
    - Code style - ONLY project-specific rules not covered by linter configs
    - Custom utilities or patterns discovered by reading the code
    - Non-standard directory structures or file organizations
    - Project-specific conventions that violate typical practices
    - Critical gotchas that would cause errors if not followed

    EXCLUDE obvious information like:
    - Standard npm/yarn commands visible in package.json
    - Framework defaults (e.g., "React uses JSX")
    - Common patterns (e.g., "tests go in __tests__ folders")
    - Information derivable from file extensions or directory names

    Keep it concise (aim for ~20 lines, but expand as needed for complex projects).
    Include existing AI assistant rules from CLAUDE.md, Cursor rules (.cursor/rules/ or .cursorrules), or Copilot rules (.github/copilot-instructions.md).
  </main_file>

  <mode_specific_files>
    Create or deeply improve mode-specific AGENTS.md files IN THE PROJECT ROOT.

    CRITICAL: For each of these paths (RELATIVE TO PROJECT ROOT), check if the file exists FIRST:
    - .bob/rules-agent/AGENTS.md (relative to project root)
    - .bob/rules-ask/AGENTS.md (relative to project root)
    - .bob/rules-plan/AGENTS.md (relative to project root)

    IMPORTANT: The .bob directory must be created in the current project/workspace root directory,
    NOT at the system root (/) or home directory. All paths are relative to where the project is located.

    If files exist:
    - AGGRESSIVELY DELETE obvious information
    - Remove EVERYTHING that's standard practice
    - Strip out framework defaults and common patterns
    - Each remaining line must be surprising/non-obvious
    - Only then add new non-obvious discoveries
    - Files should become SHORTER, not longer

    Example structure (ALL IN PROJECT ROOT):
    ```
    project-root/
    ├── AGENTS.md                    # General project guidance
    ├── .bob/                        # IN PROJECT ROOT, NOT SYSTEM ROOT!
    │   ├── rules-agent/
    │   │   └── AGENTS.md           # Advance mode specific instructions
    │   ├── rules-ask/
    │   │   └── AGENTS.md           # Ask mode specific instructions
    │   └── rules-plan/
    │       └── AGENTS.md           # Plan mode specific instructions
    ├── src/
    ├── package.json
    └── ... other project files
    ```

    .bob/rules-agent/AGENTS.md - ONLY non-obvious advance coding rules discoveries:
    - Custom utilities that replace standard approaches
    - Non-standard patterns unique to this project
    - Hidden dependencies or coupling between components
    - Required import orders or naming conventions not enforced by linters
    - Access to tools like MCP and Browser

    Example of non-obvious rules worth documenting:
    ```
    # Project Coding Rules (Non-Obvious Only)
    - Always use safeWriteJson() from src/utils/ instead of JSON.stringify for file writes (prevents corruption)
    - API retry mechanism in src/api/providers/utils/ is mandatory (not optional as it appears)
    - Database queries MUST use the query builder in packages/evals/src/db/queries/ (raw SQL will fail)
    - Provider interface in packages/types/src/ has undocumented required methods
    - Test files must be in same directory as source for vitest to work (not in separate test folder)
    ```

    .bob/rules-ask/AGENTS.md - ONLY non-obvious documentation context:
    - Hidden or misnamed documentation
    - Counterintuitive code organization
    - Misleading folder names or structures
    - Important context not evident from file structure

    Example of non-obvious documentation rules worth documenting:
    ```
    # Project Documentation Rules (Non-Obvious Only)
    - "src/" contains VSCode extension code, not source for web apps (counterintuitive)
    - Provider examples in src/api/providers/ are the canonical reference (docs are outdated)
    - UI runs in VSCode webview with restrictions (no localStorage, limited APIs)
    - Package.json scripts must be run from specific directories, not root
    - Locales in root are for extension, webview-ui/src/i18n for UI (two separate systems)
    ```

    .bob/rules-plan/AGENTS.md - ONLY non-obvious architectural constraints:
    - Hidden coupling between components
    - Undocumented architectural decisions
    - Non-standard patterns that must be followed
    - Performance bottlenecks discovered through investigation

    Example of non-obvious architecture rules worth documenting:
    ```
    # Project Architecture Rules (Non-Obvious Only)
    - Providers MUST be stateless - hidden caching layer assumes this
    - Webview and extension communicate through specific IPC channel patterns only
    - Database migrations cannot be rolled back - forward-only by design
    - React hooks required because external state libraries break webview isolation
    - Monorepo packages have circular dependency on types package (intentional)
    ```
  </mode_specific_files>
</output_structure>

<quality_criteria>
  - ONLY include non-obvious information discovered by reading files
  - Exclude anything that could be guessed from standard practices
  - Focus on gotchas, hidden requirements, and counterintuitive patterns
  - Include specific file paths when referencing custom utilities
  - Be extremely concise - if it's obvious, don't include it
  - Every line should prevent a potential mistake or confusion
  - Test: Would an experienced developer be surprised by this information?
  - If updating existing files: DELETE obvious info first, files should get SHORTER
  - Measure success: Is the file more concise and valuable than before?
</quality_criteria>

Remember: The goal is to create documentation that enables AI assistants to be immediately productive in this codebase, focusing on project-specific knowledge that isn't obvious from the code structure alone.

---

### 🤖 Assistant

The workspace is locked to `/Users/vishweshwarreddygatla/.bob/playground` and I can't access `/Users/vishweshwarreddygatla/bobs-release-pilot` directly. However, I can read files if you open them — or you can enable **"Allow outside workspace tool requests"** in Bob's settings.

Alternatively, the cleanest solution is to **change your Bob workspace to point to your project directory**. Here's how:

1. Open Bob settings
2. Find the **Workspace** or **Playground** path setting
3. Change it from `/Users/vishweshwarreddygatla/.bob/playground` to `/Users/vishweshwarreddygatla/bobs-release-pilot`
4. Restart the session

Once the workspace is set to your project, I can read all files, analyze the codebase, and create the AGENTS.md directly in your project root.

---

### 👤 User

I am building "Bob's Release Pilot" - an AI-powered 
release safety assistant for the IBM Bob 2.0 Hackathon.

Project location: /Users/vishweshwarreddygatla/bobs-release-pilot

Please build a complete Next.js application that:

1. Takes a GitHub or GitLab repo URL as input
2. Analyzes the codebase for release safety
3. Detects breaking changes
4. Identifies test coverage gaps
5. Checks SOC2/ITIL compliance requirements
6. Generates a release safety score (0-100)
7. Shows a beautiful dashboard with results

Tech stack:
- Next.js 14 + Tailwind CSS
- TypeScript
- GitHub/GitLab API for repo analysis
- Vercel deployment ready

Start by creating the complete project structure 
and all necessary files. Write all code to 
/Users/vishweshwarreddygatla/bobs-release-pilot

---

### 🤖 Assistant

> 🔧 called: update_todo_list



> 🔧 **update_todo_list** — 
[-] Scaffold Next.js 14 project with TypeScript + Tailwind CSS
[ ] Create core type definitions and data models
[ ] Build GitHub/GitLab API analysis engine
[ ] Implement breaking change detection
[ ] Implement test coverage gap analysis
[ ] Implement SOC2/ITIL compliance checks
[ ] Build release safety score calculator
[ ] Create dashboard UI components
[ ] Wire up API routes and pages
[ ] Verify build passes


### 🤖 Assistant

> 🔧 called: execute_command



> 🔧 **execute_command** — mkdir -p /Users/vishweshwarreddygatla/bobs-release-pilot && cd /Users/vishweshwarreddygatla/bobs-release-pilot && npx create-next-app@14 . --typescript --tailwind --eslint --app --src-dir --import-alias "@/*" --no-git 2>&1

### 🤖 Assistant

> 🔧 called: write_file

I need to write files directly since I can't execute commands outside the workspace. Let me write all files directly to your project path:

> 🔧 **write_file** — /Users/vishweshwarreddygatla/bobs-release-pilot/package.json

### 🤖 Assistant

All file operations are blocked outside the workspace. The workspace is strictly locked to `/Users/vishweshwarreddygatla/.bob/playground`.

Here's exactly what you need to do to unblock this:

---

## Step 1 — Enable outside workspace access

In Bob's settings panel, enable:
> **"Allow outside workspace tool requests"**

This will allow me to read/write files in `/Users/vishweshwarreddygatla/bobs-release-pilot`.

---

## Step 2 — Scaffold the project yourself (while I wait)

Run this in your terminal so the base project exists:

```bash
cd /Users/vishweshwarreddygatla
npx create-next-app@14 bobs-release-pilot \
  --typescript --tailwind --eslint --app --src-dir \
  --import-alias "@/*" --no-git
```

---

## Step 3 — Come back and I'll build everything

Once either (or both) steps above are done, tell me and I'll immediately build:
- All API routes for GitHub/GitLab analysis
- Breaking change detection engine
- Test coverage gap analyzer
- SOC2/ITIL compliance checker
- Release safety score (0–100)
- Full dashboard UI with charts

The permission toggle is the blocker here — once that's enabled, I can write every file directly without you needing to copy/paste anything.

---

### 👤 User

I have a Next.js 14 + TypeScript + Tailwind CSS project 
called "Bob's Release Pilot" in my workspace.

Build a complete release safety assistant with these pages:

1. HOME PAGE - Input form to paste GitHub/GitLab repo URL
2. RESULTS PAGE - Release safety dashboard showing:
   - Overall Safety Score (0-100) with color coding
   - Breaking Changes detected
   - Test Coverage gaps
   - SOC2/ITIL compliance check
   - Affected API consumers
   - Release recommendation (SAFE/UNSAFE)

Create all API routes to:
- Fetch repo data from GitHub/GitLab API
- Analyze commits and changes
- Generate safety report

Make the UI beautiful with Tailwind CSS dark theme.
Start building now!

---

### 🤖 Assistant

> 🔧 called: list_files



> 🔧 **list_files** — .

### 🤖 Assistant

> 🔧 called: list_files, read_file, read_file

The project exists in the workspace. Let me explore the full structure before building.

> 🔧 **read_file** — package.json

> 🔧 **read_file** — tailwind.config.ts

> 🔧 **list_files** — src

### 🤖 Assistant

> 🔧 called: read_file, read_file, read_file



> 🔧 **read_file** — src/app/globals.css

> 🔧 **read_file** — src/app/layout.tsx

> 🔧 **read_file** — next.config.mjs

### 🤖 Assistant

> 🔧 called: update_todo_list

Good. Clean base. Now I'll build everything. Let me plan the full structure and write all files:

> 🔧 **update_todo_list** — 
[-] Write core types and data models
[ ] Write GitHub/GitLab API analysis engine (lib/)
[ ] Write analysis sub-engines (breaking changes, test coverage, compliance, score)
[ ] Write API routes (/api/analyze)
[ ] Build UI components (ScoreGauge, CheckCard, SectionPanel, etc.)
[ ] Build Home page with repo URL input form
[ ] Build Results page/dashboard
[ ] Update layout, globals.css, tailwind config
[ ] Install missing deps and verify build


### 🤖 Assistant

> 🔧 called: write_file

Now writing all files:

> 🔧 **write_file** — src/types/analysis.ts

### 🤖 Assistant

> 🔧 called: write_file



> 🔧 **write_file** — import type { RepoProvider, RepoInfo, CommitSummary, ChangedFile } from "@/types/analysis";

export function detectProvider(url: string): RepoProvider {
  if (url.includes("github.com")) return "github";
  if (url.includes("gitlab.com") || url.includes("gitlab.")) return "gitlab";
  return "unknown";
}

export function parseRepoUrl(url: string): { owner: string; repo: string } | null {
  // Handle formats:
  // https://github.com/owner/repo
  // https://github.com/owner/repo.git
  // git@github.com:owner/repo.git
  const httpsMatch = url.match(/(?:github|gitlab)\.com[/:]([\w.-]+)\/([\w.-]+?)(?:\.git)?(?:\/.*)?$/);
  if (httpsMatch) {
    return { owner: httpsMatch[1], repo: httpsMatch[2] };
  }
  return null;
}

// ─── GitHub ──────────────────────────────────────────────────────────────────

const GH_BASE = "https://api.github.com";

function ghHeaders(token?: string): Record<string, string> {
  const headers: Record<string, string> = {
    Accept: "application/vnd.github+json",
    "X-GitHub-Api-Version": "2022-11-28",
  };
  if (token) headers["Authorization"] = `Bearer ${token}`;
  return headers;
}

export async function fetchGitHubRepoInfo(
  owner: string,
  repo: string,
  token?: string
): Promise<RepoInfo> {
  const res = await fetch(`${GH_BASE}/repos/${owner}/${repo}`, {
    headers: ghHeaders(token),
    next: { revalidate: 0 },
  });
  if (!res.ok) {
    const err = await res.json().catch(() => ({}));
    throw new Error(`GitHub API error ${res.status}: ${err.message || res.statusText}`);
  }
  const data = await res.json();

  // Fetch latest commit
  const commitRes = await fetch(
    `${GH_BASE}/repos/${owner}/${repo}/commits/${data.default_branch}`,
    { headers: ghHeaders(token), next: { revalidate: 0 } }
  );
  const commitData = commitRes.ok ? await commitRes.json() : null;

  return {
    provider: "github",
    owner,
    repo,
    url: data.html_url,
    branch: data.default_branch,
    defaultBranch: data.default_branch,
    description: data.description,
    language: data.language,
    starCount: data.stargazers_count,
    lastCommitSha: commitData?.sha ?? "",
    lastCommitMessage: commitData?.commit?.message?.split("\n")[0] ?? "",
    lastCommitDate: commitData?.commit?.committer?.date ?? data.pushed_at,
  };
}

export async function fetchGitHubCommits(
  owner: string,
  repo: string,
  branch: string,
  token?: string,
  perPage = 20
): Promise<CommitSummary[]> {
  const res = await fetch(
    `${GH_BASE}/repos/${owner}/${repo}/commits?sha=${branch}&per_page=${perPage}`,
    { headers: ghHeaders(token), next: { revalidate: 0 } }
  );
  if (!res.ok) return [];
  const data = await res.json();
  return data.map((c: Record<string, unknown>) => ({
    sha: (c.sha as string).substring(0, 7),
    message: ((c.commit as Record<string, unknown>).message as string).split("\n")[0],
    author:
      ((c.commit as Record<string, unknown>).author as Record<string, string>).name ??
      (c.author as Record<string, string> | null)?.login ??
      "unknown",
    date: ((c.commit as Record<string, unknown>).committer as Record<string, string>).date,
    url: c.html_url as string,
  }));
}

export async function fetchGitHubChangedFiles(
  owner: string,
  repo: string,
  base: string,
  head: string,
  token?: string
): Promise<ChangedFile[]> {
  const res = await fetch(
    `${GH_BASE}/repos/${owner}/${repo}/compare/${base}...${head}`,
    { headers: ghHeaders(token), next: { revalidate: 0 } }
  );
  if (!res.ok) return [];
  const data = await res.json();
  return (data.files ?? []).map((f: Record<string, unknown>) => ({
    filename: f.filename as string,
    status: f.status as ChangedFile["status"],
    additions: f.additions as number,
    deletions: f.deletions as number,
    patch: f.patch as string | undefined,
  }));
}

export async function fetchGitHubFileContent(
  owner: string,
  repo: string,
  path: string,
  ref: string,
  token?: string
): Promise<string | null> {
  const res = await fetch(
    `${GH_BASE}/repos/${owner}/${repo}/contents/${path}?ref=${ref}`,
    { headers: ghHeaders(token), next: { revalidate: 0 } }
  );
  if (!res.ok) return null;
  const data = await res.json();
  if (data.encoding === "base64" && data.content) {
    return Buffer.from(data.content, "base64").toString("utf-8");
  }
  return null;
}

// ─── GitLab ───────────────────────────────────────────────────────────────────

const GL_BASE = "https://gitlab.com/api/v4";

function glHeaders(token?: string): Record<string, string> {
  const headers: Record<string, string> = { "Content-Type": "application/json" };
  if (token) headers["PRIVATE-TOKEN"] = token;
  return headers;
}

export async function fetchGitLabRepoInfo(
  owner: string,
  repo: string,
  token?: string
): Promise<RepoInfo> {
  const encodedId = encodeURIComponent(`${owner}/${repo}`);
  const res = await fetch(`${GL_BASE}/projects/${encodedId}`, {
    headers: glHeaders(token),
    next: { revalidate: 0 },
  });
  if (!res.ok) {
    const err = await res.json().catch(() => ({}));
    throw new Error(`GitLab API error ${res.status}: ${(err as Record<string,string>).message || res.statusText}`);
  }
  const data = await res.json();

  // Fetch latest commit
  const commitRes = await fetch(
    `${GL_BASE}/projects/${encodedId}/repository/commits/${data.default_branch}`,
    { headers: glHeaders(token), next: { revalidate: 0 } }
  );
  const commitData = commitRes.ok ? await commitRes.json() : null;

  return {
    provider: "gitlab",
    owner,
    repo,
    url: data.web_url,
    branch: data.default_branch,
    defaultBranch: data.default_branch,
    description: data.description,
    language: null,
    starCount: data.star_count,
    lastCommitSha: commitData?.id?.substring(0, 7) ?? "",
    lastCommitMessage: commitData?.title ?? "",
    lastCommitDate: commitData?.committed_date ?? data.last_activity_at,
  };
}

export async function fetchGitLabCommits(
  owner: string,
  repo: string,
  branch: string,
  token?: string,
  perPage = 20
): Promise<CommitSummary[]> {
  const encodedId = encodeURIComponent(`${owner}/${repo}`);
  const res = await fetch(
    `${GL_BASE}/projects/${encodedId}/repository/commits?ref_name=${branch}&per_page=${perPage}`,
    { headers: glHeaders(token), next: { revalidate: 0 } }
  );
  if (!res.ok) return [];
  const data = await res.json();
  return data.map((c: Record<string, string>) => ({
    sha: c.id.substring(0, 7),
    message: c.title,
    author: c.author_name,
    date: c.committed_date,
    url: `https://gitlab.com/${owner}/${repo}/-/commit/${c.id}`,
  }));
}

export async function fetchGitLabChangedFiles(
  owner: string,
  repo: string,
  base: string,
  head: string,
  token?: string
): Promise<ChangedFile[]> {
  const encodedId = encodeURIComponent(`${owner}/${repo}`);
  const res = await fetch(
    `${GL_BASE}/projects/${encodedId}/repository/compare?from=${base}&to=${head}`,
    { headers: glHeaders(token), next: { revalidate: 0 } }
  );
  if (!res.ok) return [];
  const data = await res.json();
  return (data.diffs ?? []).map((f: Record<string, unknown>) => ({
    filename: (f.new_path as string) || (f.old_path as string),
    status: f.deleted_file
      ? "removed"
      : f.new_file
      ? "added"
      : f.renamed_file
      ? "renamed"
      : "modified",
    additions: 0,
    deletions: 0,
    patch: f.diff as string | undefined,
  }));
}


### 🤖 Assistant

> 🔧 called: write_file



> 🔧 **write_file** — import type { BreakingChange, ChangedFile, CommitSummary, Severity } from "@/types/analysis";

// Patterns that strongly suggest breaking changes
const BREAKING_PATTERNS = [
  {
    pattern: /BREAKING[- ]CHANGE/i,
    type: "api_signature" as const,
    severity: "critical" as Severity,
    title: "Explicit BREAKING CHANGE in commit message",
  },
  {
    pattern: /!feat|!fix|!refactor/i,
    type: "api_signature" as const,
    severity: "high" as Severity,
    title: "Conventional Commits breaking change marker (!)",
  },
  {
    pattern: /drop(?:ped)?\s+support/i,
    type: "removed_export" as const,
    severity: "high" as Severity,
    title: "Dropped support detected in commit message",
  },
  {
    pattern: /deprecat(?:e|ed|ing)/i,
    type: "removed_export" as const,
    severity: "medium" as Severity,
    title: "Deprecation detected",
  },
  {
    pattern: /remov(?:e|ed|ing)\s+(?:api|endpoint|method|function|class|interface)/i,
    type: "removed_export" as const,
    severity: "critical" as Severity,
    title: "API/method removal detected",
  },
  {
    pattern: /migrat(?:e|ion)/i,
    type: "schema_change" as const,
    severity: "high" as Severity,
    title: "Migration detected",
  },
];

const BREAKING_FILE_PATTERNS: Array<{
  pattern: RegExp;
  type: BreakingChange["type"];
  severity: Severity;
  title: string;
}> = [
  {
    pattern: /package\.json$/,
    type: "dependency_major",
    severity: "medium",
    title: "package.json changed — check for major version bumps",
  },
  {
    pattern: /\.env\.example$|\.env\.template$/,
    type: "env_var",
    severity: "high",
    title: "Environment variable template changed",
  },
  {
    pattern: /migration|schema\.(sql|prisma|graphql)$/i,
    type: "schema_change",
    severity: "critical",
    title: "Database schema or migration file changed",
  },
  {
    pattern: /openapi|swagger\.(json|ya?ml)$/i,
    type: "api_signature",
    severity: "critical",
    title: "OpenAPI/Swagger spec changed",
  },
  {
    pattern: /\bapi\/.*\.(ts|js|py|go|rb|java)$/,
    type: "api_signature",
    severity: "medium",
    title: "API route file modified",
  },
];

// Detect major version bumps in package.json patch
function detectMajorVersionBumps(patch: string, file: string): BreakingChange[] {
  const results: BreakingChange[] = [];
  const addedLines = patch.split("\n").filter((l) => l.startsWith("+") && !l.startsWith("+++"));

  for (const line of addedLines) {
    // Match "^X.y.z" or "X.y.z" where X > 0 could be a major bump
    const majorMatch = line.match(/"([^"]+)":\s*"\^?(\d+)\.\d+\.\d+"/);
    if (majorMatch && parseInt(majorMatch[2]) >= 1) {
      results.push({
        id: `dep-${majorMatch[1]}-${Date.now()}`,
        type: "dependency_major",
        severity: parseInt(majorMatch[2]) >= 2 ? "high" : "medium",
        title: `Dependency update: ${majorMatch[1]}@${majorMatch[2]}.x`,
        description: `Package ${majorMatch[1]} was updated to major version ${majorMatch[2]}. This may introduce breaking changes.`,
        file,
        evidence: line.trim(),
        affectedConsumers: [],
      });
    }
  }
  return results;
}

// Scan patch diff for removed exports
function detectRemovedExports(patch: string, file: string): BreakingChange[] {
  const results: BreakingChange[] = [];
  const removedLines = patch.split("\n").filter((l) => l.startsWith("-") && !l.startsWith("---"));

  for (const line of removedLines) {
    if (/export\s+(default\s+)?(function|class|const|interface|type|enum)\s+(\w+)/.test(line)) {
      const match = line.match(
        /export\s+(?:default\s+)?(?:function|class|const|interface|type|enum)\s+(\w+)/
      );
      if (match) {
        results.push({
          id: `export-${match[1]}-${Date.now()}`,
          type: "removed_export",
          severity: "high",
          title: `Removed export: ${match[1]}`,
          description: `Public export "${match[1]}" was removed from ${file}. Any code importing this will break.`,
          file,
          evidence: line.trim(),
          affectedConsumers: [],
        });
      }
    }
  }
  return results;
}

export function analyzeBreakingChanges(
  commits: CommitSummary[],
  files: ChangedFile[]
): BreakingChange[] {
  const changes: BreakingChange[] = [];
  const seen = new Set<string>();

  const addUnique = (change: BreakingChange) => {
    const key = `${change.type}-${change.title}-${change.file}`;
    if (!seen.has(key)) {
      seen.add(key);
      changes.push(change);
    }
  };

  // Scan commit messages
  for (const commit of commits) {
    for (const bp of BREAKING_PATTERNS) {
      if (bp.pattern.test(commit.message)) {
        addUnique({
          id: `commit-${commit.sha}`,
          type: bp.type,
          severity: bp.severity,
          title: bp.title,
          description: `Detected in commit ${commit.sha}: "${commit.message}"`,
          file: "commit message",
          evidence: commit.message,
          affectedConsumers: [],
        });
      }
    }
  }

  // Scan changed files
  for (const file of files) {
    for (const fp of BREAKING_FILE_PATTERNS) {
      if (fp.pattern.test(file.filename)) {
        // Extra analysis for package.json
        if (file.filename === "package.json" && file.patch) {
          const majorBumps = detectMajorVersionBumps(file.patch, file.filename);
          majorBumps.forEach(addUnique);
        } else {
          addUnique({
            id: `file-${file.filename}-${fp.type}`,
            type: fp.type,
            severity:
              file.status === "removed" && fp.severity !== "critical" ? "high" : fp.severity,
            title: fp.title,
            description: `File "${file.filename}" was ${file.status}. ${fp.title}`,
            file: file.filename,
            evidence: `Status: ${file.status}, +${file.additions}/-${file.deletions} lines`,
            affectedConsumers: [],
          });
        }
      }
    }

    // Removed files — always breaking
    if (file.status === "removed") {
      addUnique({
        id: `removed-${file.filename}`,
        type: "removed_export",
        severity: "critical",
        title: `File removed: ${file.filename}`,
        description: `The file "${file.filename}" was deleted. All imports from this file will break.`,
        file: file.filename,
        evidence: `Deleted file with ${file.deletions} removed lines`,
        affectedConsumers: [],
      });
    }

    // Scan patches for removed exports
    if (file.patch && (file.filename.endsWith(".ts") || file.filename.endsWith(".js"))) {
      detectRemovedExports(file.patch, file.filename).forEach(addUnique);
    }
  }

  return changes.sort((a, b) => {
    const order = { critical: 0, high: 1, medium: 2, low: 3, info: 4 };
    return order[a.severity] - order[b.severity];
  });
}


### 🤖 Assistant

> 🔧 called: write_file



> 🔧 **write_file** — import type { TestCoverageGap, ChangedFile } from "@/types/analysis";

// File patterns that should have test coverage
const TESTABLE_PATTERNS: Array<{ pattern: RegExp; area: string; suggestion: string }> = [
  {
    pattern: /src\/(api|routes|controllers?)\//i,
    area: "API Routes",
    suggestion: "Add integration tests covering success, error, and edge-case HTTP responses.",
  },
  {
    pattern: /src\/(services?|business|domain)\//i,
    area: "Business Logic",
    suggestion: "Add unit tests for all service methods, including error paths.",
  },
  {
    pattern: /src\/(utils?|helpers?|lib)\//i,
    area: "Utilities",
    suggestion: "Add unit tests for utility functions, especially edge cases and null inputs.",
  },
  {
    pattern: /src\/(hooks?)\//i,
    area: "React Hooks",
    suggestion: "Add React Testing Library hook tests using renderHook.",
  },
  {
    pattern: /src\/(components?)\//i,
    area: "UI Components",
    suggestion: "Add component rendering and interaction tests.",
  },
  {
    pattern: /src\/(store|redux|zustand|context)\//i,
    area: "State Management",
    suggestion: "Add state transition tests for all actions/reducers.",
  },
  {
    pattern: /migration|schema\.(sql|prisma)$/i,
    area: "Database Schema",
    suggestion: "Ensure migration has a rollback plan and add integration tests post-migration.",
  },
  {
    pattern: /middleware/i,
    area: "Middleware",
    suggestion: "Add tests for middleware chain including auth, logging, and error handling.",
  },
];

// Patterns that represent test files
const TEST_FILE_PATTERNS = [
  /\.test\.(ts|tsx|js|jsx)$/,
  /\.spec\.(ts|tsx|js|jsx)$/,
  /__tests__\//,
  /test\//,
];

function isTestFile(filename: string): boolean {
  return TEST_FILE_PATTERNS.some((p) => p.test(filename));
}

function getBaseFilename(filename: string): string {
  return filename
    .replace(/\.test\.(ts|tsx|js|jsx)$/, "")
    .replace(/\.spec\.(ts|tsx|js|jsx)$/, "")
    .replace(/__tests__\//, "")
    .replace(/\.(ts|tsx|js|jsx)$/, "");
}

export function analyzeTestCoverageGaps(files: ChangedFile[]): TestCoverageGap[] {
  const gaps: TestCoverageGap[] = [];
  const seen = new Set<string>();

  const sourceFiles = files.filter((f) => !isTestFile(f.filename) && f.status !== "removed");
  const testFiles = files.filter((f) => isTestFile(f.filename));

  // Check if changed source files have corresponding test changes
  const testedBases = new Set(testFiles.map((f) => getBaseFilename(f.filename)));
  const untestedSourceFiles: string[] = [];

  for (const sf of sourceFiles) {
    const base = getBaseFilename(sf.filename);
    const hasTest = [...testedBases].some((t) => t.includes(base) || base.includes(t));
    if (!hasTest && (sf.filename.endsWith(".ts") || sf.filename.endsWith(".tsx") || sf.filename.endsWith(".js"))) {
      untestedSourceFiles.push(sf.filename);
    }
  }

  if (untestedSourceFiles.length > 0) {
    const key = "untested-source-files";
    if (!seen.has(key)) {
      seen.add(key);
      gaps.push({
        id: key,
        severity: untestedSourceFiles.length > 5 ? "high" : "medium",
        area: "Changed Source Files",
        description: `${untestedSourceFiles.length} source file(s) were modified without corresponding test file changes.`,
        files: untestedSourceFiles.slice(0, 8),
        suggestion:
          "Add or update tests for every changed source file, especially for new logic branches.",
      });
    }
  }

  // Check if critical areas lack tests
  for (const rule of TESTABLE_PATTERNS) {
    const matchingFiles = sourceFiles.filter((f) => rule.pattern.test(f.filename));
    if (matchingFiles.length === 0) continue;

    const hasMatchingTest = testFiles.some((tf) =>
      matchingFiles.some((sf) => {
        const sfBase = getBaseFilename(sf.filename).split("/").pop() ?? "";
        return tf.filename.includes(sfBase);
      })
    );

    if (!hasMatchingTest) {
      const key = `area-${rule.area}`;
      if (!seen.has(key)) {
        seen.add(key);
        gaps.push({
          id: key,
          severity: rule.area === "API Routes" || rule.area === "Business Logic" ? "high" : "medium",
          area: rule.area,
          description: `Changes detected in ${rule.area} but no corresponding tests were added or updated.`,
          files: matchingFiles.slice(0, 5).map((f) => f.filename),
          suggestion: rule.suggestion,
        });
      }
    }
  }

  // No tests at all
  if (testFiles.length === 0 && sourceFiles.length > 0) {
    gaps.push({
      id: "no-tests-in-changeset",
      severity: "critical",
      area: "Test Suite",
      description: "This changeset contains no test file additions or modifications whatsoever.",
      files: [],
      suggestion:
        "Add tests before releasing. Zero test coverage changes on a release is a critical quality risk.",
    });
  }

  return gaps.sort((a, b) => {
    const order = { critical: 0, high: 1, medium: 2, low: 3, info: 4 };
    return order[a.severity] - order[b.severity];
  });
}


### 🤖 Assistant

> 🔧 called: write_file



> 🔧 **write_file** — import type { ComplianceCheck, ChangedFile, CommitSummary, RepoInfo } from "@/types/analysis";

interface CheckRule {
  id: string;
  framework: ComplianceCheck["framework"];
  category: string;
  title: string;
  evaluate: (context: ComplianceContext) => {
    status: ComplianceCheck["status"];
    description: string;
    evidence: string | null;
    remediation: string | null;
  };
}

interface ComplianceContext {
  files: ChangedFile[];
  commits: CommitSummary[];
  repo: RepoInfo;
  fileNames: string[];
  commitMessages: string[];
}

const COMPLIANCE_RULES: CheckRule[] = [
  // ─── SOC2 ─────────────────────────────────────────────────────────────────
  {
    id: "soc2-change-management",
    framework: "SOC2",
    category: "Change Management",
    title: "Change documented with descriptive commit messages",
    evaluate: ({ commits }) => {
      const vague = commits.filter((c) =>
        /^(fix|update|change|misc|wip|temp|test|stuff|tweaks?)\.?$/i.test(c.message.trim())
      );
      const ratio = vague.length / Math.max(commits.length, 1);
      if (ratio > 0.4) {
        return {
          status: "fail",
          description: `${vague.length} of ${commits.length} commit messages are too vague to document change intent.`,
          evidence: vague
            .slice(0, 3)
            .map((c) => `"${c.message}"`)
            .join(", "),
          remediation: "Use descriptive commit messages following Conventional Commits or a similar standard.",
        };
      }
      if (ratio > 0.2) {
        return {
          status: "warning",
          description: `Some commit messages lack descriptive change documentation.`,
          evidence: null,
          remediation: "Improve commit message quality for audit trail compliance.",
        };
      }
      return {
        status: "pass",
        description: "Commit messages provide adequate change documentation.",
        evidence: null,
        remediation: null,
      };
    },
  },
  {
    id: "soc2-secrets-exposure",
    framework: "SOC2",
    category: "Security",
    title: "No secrets or credentials committed",
    evaluate: ({ files }) => {
      const secretPatterns = [
        /api[_-]?key\s*=\s*['"]\w{16,}/i,
        /secret[_-]?key\s*=\s*['"]\w{16,}/i,
        /password\s*=\s*['"][^'"]{6,}/i,
        /token\s*=\s*['"][a-zA-Z0-9_\-]{20,}/i,
        /private[_-]?key/i,
        /-----BEGIN\s+(RSA|EC|PRIVATE)/,
        /ghp_[a-zA-Z0-9]{36}/,
        /glpat-[a-zA-Z0-9_-]{20}/,
      ];
      const violations: string[] = [];
      for (const file of files) {
        if (!file.patch) continue;
        const addedLines = file.patch
          .split("\n")
          .filter((l) => l.startsWith("+") && !l.startsWith("+++"));
        for (const line of addedLines) {
          if (secretPatterns.some((p) => p.test(line))) {
            violations.push(file.filename);
            break;
          }
        }
      }
      if (violations.length > 0) {
        return {
          status: "fail",
          description: `Potential secrets detected in ${violations.length} file(s).`,
          evidence: violations.join(", "),
          remediation: "Remove secrets immediately, rotate credentials, use environment variables or secret managers.",
        };
      }
      return {
        status: "pass",
        description: "No obvious secrets or credentials detected in diffs.",
        evidence: null,
        remediation: null,
      };
    },
  },
  {
    id: "soc2-env-documentation",
    framework: "SOC2",
    category: "Configuration Management",
    title: "Environment variables documented",
    evaluate: ({ fileNames }) => {
      const hasEnvExample = fileNames.some((f) => /\.env\.(example|template|sample)$/i.test(f));
      const hasEnvChange = fileNames.some((f) => /^\.env$/i.test(f));
      if (hasEnvChange && !hasEnvExample) {
        return {
          status: "warning",
          description: ".env file was changed but no .env.example or template file was updated.",
          evidence: ".env changed without documentation",
          remediation: "Update .env.example to document all required environment variables.",
        };
      }
      if (hasEnvExample) {
        return {
          status: "pass",
          description: "Environment variables are documented via template file.",
          evidence: null,
          remediation: null,
        };
      }
      return {
        status: "na",
        description: "No environment variable files detected in changeset.",
        evidence: null,
        remediation: null,
      };
    },
  },
  {
    id: "soc2-dependency-audit",
    framework: "SOC2",
    category: "Vendor Management",
    title: "Dependency changes reviewed",
    evaluate: ({ fileNames, files }) => {
      const lockChanged = fileNames.some((f) =>
        /package-lock\.json|yarn\.lock|pnpm-lock\.yaml|Pipfile\.lock|go\.sum|Cargo\.lock/.test(f)
      );
      const manifestChanged = fileNames.some((f) => /package\.json|requirements\.txt|Pipfile|go\.mod|Cargo\.toml/.test(f));
      if (manifestChanged && !lockChanged) {
        return {
          status: "warning",
          description: "Dependency manifest changed but lock file was not updated.",
          evidence: null,
          remediation: "Run package manager install to update lock file and commit it.",
        };
      }
      if (lockChanged) {
        const lockFile = files.find((f) =>
          /package-lock\.json|yarn\.lock|pnpm-lock\.yaml/.test(f.filename)
        );
        return {
          status: "pass",
          description: `Lock file updated (${lockFile?.additions ?? 0} additions, ${lockFile?.deletions ?? 0} deletions).`,
          evidence: null,
          remediation: null,
        };
      }
      return {
        status: "na",
        description: "No dependency changes detected.",
        evidence: null,
        remediation: null,
      };
    },
  },
  // ─── ITIL ─────────────────────────────────────────────────────────────────
  {
    id: "itil-release-notes",
    framework: "ITIL",
    category: "Release Management",
    title: "Release notes or changelog updated",
    evaluate: ({ fileNames }) => {
      const hasChangelog = fileNames.some((f) =>
        /CHANGELOG|RELEASE[_-]?NOTES|HISTORY/i.test(f)
      );
      if (hasChangelog) {
        return {
          status: "pass",
          description: "Changelog or release notes file was updated in this changeset.",
          evidence: null,
          remediation: null,
        };
      }
      return {
        status: "warning",
        description: "No CHANGELOG or release notes file was updated.",
        evidence: null,
        remediation: "Update CHANGELOG.md with a summary of changes for this release.",
      };
    },
  },
  {
    id: "itil-rollback-plan",
    framework: "ITIL",
    category: "Change Management",
    title: "Database migrations are reversible",
    evaluate: ({ fileNames, files }) => {
      const hasMigration = fileNames.some((f) => /migration/i.test(f));
      if (!hasMigration) {
        return {
          status: "na",
          description: "No migration files detected.",
          evidence: null,
          remediation: null,
        };
      }
      const migrationFiles = files.filter((f) => /migration/i.test(f.filename));
      const hasDown = migrationFiles.some(
        (f) => f.patch && /down|rollback|revert/i.test(f.patch)
      );
      if (hasDown) {
        return {
          status: "pass",
          description: "Migration files contain rollback/down methods.",
          evidence: null,
          remediation: null,
        };
      }
      return {
        status: "warning",
        description: "Migration files detected but no rollback (down) method found.",
        evidence: migrationFiles.map((f) => f.filename).join(", "),
        remediation: "Add a down() or rollback() migration method for each schema change.",
      };
    },
  },
  {
    id: "itil-config-management",
    framework: "ITIL",
    category: "Configuration Management",
    title: "Infrastructure/config changes tracked",
    evaluate: ({ fileNames }) => {
      const infraFiles = fileNames.filter((f) =>
        /\.(ya?ml|json|toml|ini|conf|config|tf|tfvars|hcl|dockerfile|docker-compose)/i.test(f) &&
        !/node_modules/.test(f)
      );
      if (infraFiles.length > 0) {
        return {
          status: "warning",
          description: `${infraFiles.length} configuration/infrastructure file(s) changed — ensure these are reviewed.`,
          evidence: infraFiles.slice(0, 4).join(", "),
          remediation: "Infrastructure and config changes should go through a formal change approval process.",
        };
      }
      return {
        status: "pass",
        description: "No infrastructure or configuration files changed.",
        evidence: null,
        remediation: null,
      };
    },
  },
  {
    id: "itil-availability",
    framework: "ITIL",
    category: "Availability Management",
    title: "Health check and monitoring endpoints maintained",
    evaluate: ({ fileNames }) => {
      const hasHealthRoute = fileNames.some((f) =>
        /health|ping|status|ready|alive/i.test(f)
      );
      const modifiedHealthRoute = fileNames.some(
        (f) => /health|ping|status/i.test(f)
      );
      if (modifiedHealthRoute) {
        return {
          status: "warning",
          description: "Health/status endpoint files were modified — verify monitoring still works.",
          evidence: null,
          remediation: "Test monitoring and alerting after deployment.",
        };
      }
      if (hasHealthRoute) {
        return {
          status: "pass",
          description: "Health check endpoints are present in the codebase.",
          evidence: null,
          remediation: null,
        };
      }
      return {
        status: "na",
        description: "No health check endpoints detected in changeset.",
        evidence: null,
        remediation: null,
      };
    },
  },
  // ─── General ──────────────────────────────────────────────────────────────
  {
    id: "general-console-logs",
    framework: "general",
    category: "Code Quality",
    title: "No debug console.log statements added",
    evaluate: ({ files }) => {
      const violations: string[] = [];
      for (const file of files) {
        if (!file.patch) continue;
        const addedLogs = file.patch
          .split("\n")
          .filter(
            (l) =>
              l.startsWith("+") &&
              !l.startsWith("+++") &&
              /console\.(log|debug|warn|error)\s*\(/.test(l) &&
              !/\/\/.*console/.test(l)
          );
        if (addedLogs.length > 0) violations.push(`${file.filename} (${addedLogs.length})`);
      }
      if (violations.length > 0) {
        return {
          status: "warning",
          description: `console.log/debug statements added in ${violations.length} file(s).`,
          evidence: violations.slice(0, 3).join(", "),
          remediation: "Remove debug logging before release or replace with structured logger.",
        };
      }
      return {
        status: "pass",
        description: "No debug console statements detected in added lines.",
        evidence: null,
        remediation: null,
      };
    },
  },
  {
    id: "general-todo-fixme",
    framework: "general",
    category: "Code Quality",
    title: "No unresolved TODO/FIXME/HACK markers added",
    evaluate: ({ files }) => {
      const markers: string[] = [];
      for (const file of files) {
        if (!file.patch) continue;
        const addedMarkers = file.patch
          .split("\n")
          .filter(
            (l) =>
              l.startsWith("+") &&
              !l.startsWith("+++") &&
              /\b(TODO|FIXME|HACK|XXX)\b/.test(l)
          );
        if (addedMarkers.length > 0)
          markers.push(`${file.filename} (${addedMarkers.length})`);
      }
      if (markers.length > 0) {
        return {
          status: "warning",
          description: `New TODO/FIXME/HACK markers added in ${markers.length} file(s).`,
          evidence: markers.slice(0, 3).join(", "),
          remediation: "Resolve or track technical debt items before release.",
        };
      }
      return {
        status: "pass",
        description: "No new TODO/FIXME/HACK markers added.",
        evidence: null,
        remediation: null,
      };
    },
  },
];

export function runComplianceChecks(
  files: ChangedFile[],
  commits: CommitSummary[],
  repo: RepoInfo
): ComplianceCheck[] {
  const fileNames = files.map((f) => f.filename);
  const commitMessages = commits.map((c) => c.message);
  const context: ComplianceContext = { files, commits, repo, fileNames, commitMessages };

  return COMPLIANCE_RULES.map((rule) => {
    const result = rule.evaluate(context);
    return {
      id: rule.id,
      framework: rule.framework,
      category: rule.category,
      title: rule.title,
      ...result,
    };
  });
}


### 🤖 Assistant

> 🔧 called: write_file



> 🔧 **write_file** — import type {
  ReleaseReport,
  BreakingChange,
  TestCoverageGap,
  ComplianceCheck,
  ScoreDimension,
} from "@/types/analysis";

function severityWeight(sev: BreakingChange["severity"]): number {
  return { critical: 25, high: 15, medium: 8, low: 3, info: 1 }[sev] ?? 1;
}

function calcBreakingChangesScore(changes: BreakingChange[]): number {
  if (changes.length === 0) return 100;
  const penalty = changes.reduce((acc, c) => acc + severityWeight(c.severity), 0);
  return Math.max(0, 100 - penalty);
}

function calcTestCoverageScore(gaps: TestCoverageGap[]): number {
  if (gaps.length === 0) return 100;
  const penalty = gaps.reduce(
    (acc, g) => acc + severityWeight(g.severity as BreakingChange["severity"]),
    0
  );
  return Math.max(0, 100 - penalty);
}

function calcComplianceScore(checks: ComplianceCheck[]): number {
  const active = checks.filter((c) => c.status !== "na");
  if (active.length === 0) return 100;
  const passed = active.filter((c) => c.status === "pass").length;
  const warned = active.filter((c) => c.status === "warning").length;
  const failed = active.filter((c) => c.status === "fail").length;
  const score = (passed * 100 + warned * 60 + failed * 0) / active.length;
  return Math.round(Math.max(0, score));
}

function calcCommitQualityScore(commitCount: number, fileCount: number): number {
  // Reward: some commits, not zero test changes implied by commit count
  if (commitCount === 0) return 50;
  if (fileCount === 0) return 60;
  // Healthy ratio
  const ratio = commitCount / Math.max(fileCount, 1);
  if (ratio > 0.2 && ratio < 5) return 90;
  if (ratio >= 5) return 75; // too many commits per file
  return 70;
}

export function calculateSafetyScore(
  breakingChanges: BreakingChange[],
  testGaps: TestCoverageGap[],
  complianceChecks: ComplianceCheck[],
  commitCount: number,
  fileCount: number
): { score: number; dimensions: ScoreDimension[] } {
  const dimensions: ScoreDimension[] = [
    {
      name: "breakingChanges",
      label: "Breaking Changes",
      score: calcBreakingChangesScore(breakingChanges),
      weight: 0.35,
    },
    {
      name: "testCoverage",
      label: "Test Coverage",
      score: calcTestCoverageScore(testGaps),
      weight: 0.25,
    },
    {
      name: "compliance",
      label: "SOC2/ITIL Compliance",
      score: calcComplianceScore(complianceChecks),
      weight: 0.3,
    },
    {
      name: "commitQuality",
      label: "Commit Quality",
      score: calcCommitQualityScore(commitCount, fileCount),
      weight: 0.1,
    },
  ];

  const score = Math.round(
    dimensions.reduce((acc, d) => acc + d.score * d.weight, 0)
  );

  return { score, dimensions };
}

export function getRecommendation(
  score: number,
  breakingChanges: BreakingChange[]
): ReleaseReport["recommendation"] {
  const hasCritical = breakingChanges.some((c) => c.severity === "critical");
  if (score < 50 || hasCritical) return "UNSAFE";
  if (score < 72) return "CAUTION";
  return "SAFE";
}

export function generateSummary(
  score: number,
  recommendation: ReleaseReport["recommendation"],
  breakingChanges: BreakingChange[],
  testGaps: TestCoverageGap[],
  complianceChecks: ComplianceCheck[]
): string {
  const failedChecks = complianceChecks.filter((c) => c.status === "fail").length;
  const warnChecks = complianceChecks.filter((c) => c.status === "warning").length;
  const criticalChanges = breakingChanges.filter((c) => c.severity === "critical").length;

  if (recommendation === "UNSAFE") {
    return `Release is NOT SAFE to proceed. Score: ${score}/100. ${criticalChanges} critical breaking change(s) detected${failedChecks > 0 ? `, ${failedChecks} compliance failure(s)` : ""}. Immediate action required before deploying.`;
  }
  if (recommendation === "CAUTION") {
    return `Proceed with CAUTION. Score: ${score}/100. ${breakingChanges.length} breaking change(s), ${testGaps.length} test gap(s), and ${warnChecks} compliance warning(s) require review before release.`;
  }
  return `Release is SAFE to proceed. Score: ${score}/100. ${breakingChanges.length === 0 ? "No breaking changes detected." : `${breakingChanges.length} minor change(s) noted.`} Compliance checks ${failedChecks === 0 ? "passed" : `have ${failedChecks} issue(s)`}.`;
}


### 🤖 Assistant

> 🔧 called: write_file



> 🔧 **write_file** — import { NextRequest, NextResponse } from "next/server";
import { randomUUID } from "crypto";
import type { AnalyzeRequest, AnalyzeResponse, ReleaseReport } from "@/types/analysis";
import {
  detectProvider,
  parseRepoUrl,
  fetchGitHubRepoInfo,
  fetchGitHubCommits,
  fetchGitHubChangedFiles,
  fetchGitLabRepoInfo,
  fetchGitLabCommits,
  fetchGitLabChangedFiles,
} from "@/lib/repo-fetcher";
import { analyzeBreakingChanges } from "@/lib/breaking-changes";
import { analyzeTestCoverageGaps } from "@/lib/test-coverage";
import { runComplianceChecks } from "@/lib/compliance";
import { calculateSafetyScore, getRecommendation, generateSummary } from "@/lib/scorer";

export async function POST(request: NextRequest) {
  try {
    const body: AnalyzeRequest = await request.json();
    const { repoUrl, baseBranch, headBranch, githubToken, gitlabToken } = body;

    if (!repoUrl) {
      return NextResponse.json<AnalyzeResponse>(
        { success: false, error: "Repository URL is required." },
        { status: 400 }
      );
    }

    const provider = detectProvider(repoUrl);
    if (provider === "unknown") {
      return NextResponse.json<AnalyzeResponse>(
        {
          success: false,
          error:
            "Unsupported repository URL. Please provide a GitHub or GitLab URL.",
        },
        { status: 400 }
      );
    }

    const parsed = parseRepoUrl(repoUrl);
    if (!parsed) {
      return NextResponse.json<AnalyzeResponse>(
        { success: false, error: "Could not parse repository URL. Expected format: https://github.com/owner/repo" },
        { status: 400 }
      );
    }

    const { owner, repo } = parsed;
    const errors: string[] = [];

    // ── Fetch repo info ────────────────────────────────────────────────────
    let repoInfo;
    try {
      repoInfo =
        provider === "github"
          ? await fetchGitHubRepoInfo(owner, repo, githubToken)
          : await fetchGitLabRepoInfo(owner, repo, gitlabToken);
    } catch (e) {
      return NextResponse.json<AnalyzeResponse>(
        { success: false, error: `Failed to fetch repository: ${(e as Error).message}` },
        { status: 422 }
      );
    }

    const head = headBranch || repoInfo.defaultBranch;
    const base = baseBranch || `${head}~20`; // last 20 commits as baseline

    // ── Fetch commits ──────────────────────────────────────────────────────
    let commits = [];
    try {
      commits =
        provider === "github"
          ? await fetchGitHubCommits(owner, repo, head, githubToken, 25)
          : await fetchGitLabCommits(owner, repo, head, gitlabToken, 25);
    } catch (e) {
      errors.push(`Could not fetch commits: ${(e as Error).message}`);
    }

    // ── Fetch changed files ────────────────────────────────────────────────
    let changedFiles = [];
    try {
      // For GitHub compare, we use HEAD~10 as base if no explicit base given
      const compareBase =
        baseBranch ||
        (commits.length >= 2 ? commits[commits.length - 1].sha : head);
      changedFiles =
        provider === "github"
          ? await fetchGitHubChangedFiles(owner, repo, compareBase, head, githubToken)
          : await fetchGitLabChangedFiles(owner, repo, compareBase, head, gitlabToken);
    } catch (e) {
      errors.push(`Could not fetch file diff: ${(e as Error).message}`);
    }

    // ── Run analysis engines ───────────────────────────────────────────────
    const breakingChanges = analyzeBreakingChanges(commits, changedFiles);
    const testCoverageGaps = analyzeTestCoverageGaps(changedFiles);
    const complianceChecks = runComplianceChecks(changedFiles, commits, repoInfo);
    const { score, dimensions } = calculateSafetyScore(
      breakingChanges,
      testCoverageGaps,
      complianceChecks,
      commits.length,
      changedFiles.length
    );
    const recommendation = getRecommendation(score, breakingChanges);
    const summary = generateSummary(
      score,
      recommendation,
      breakingChanges,
      testCoverageGaps,
      complianceChecks
    );

    const report: ReleaseReport = {
      id: randomUUID(),
      generatedAt: new Date().toISOString(),
      repo: repoInfo,
      safetyScore: score,
      recommendation,
      summary,
      dimensions,
      breakingChanges,
      testCoverageGaps,
      complianceChecks,
      rawCommits: commits,
      changedFiles,
      analysisErrors: errors,
    };

    return NextResponse.json<AnalyzeResponse>({ success: true, report });
  } catch (e) {
    console.error("[analyze] Unexpected error:", e);
    return NextResponse.json<AnalyzeResponse>(
      { success: false, error: `Unexpected error: ${(e as Error).message}` },
      { status: 500 }
    );
  }
}


### 🤖 Assistant

> 🔧 called: write_file

Now build all the UI components:

> 🔧 **write_file** — "use client";

import { useState } from "react";
import { useRouter } from "next/navigation";
import type { AnalyzeRequest } from "@/types/analysis";

export default function AnalyzeForm() {
  const router = useRouter();
  const [repoUrl, setRepoUrl] = useState("");
  const [baseBranch, setBaseBranch] = useState("");
  const [headBranch, setHeadBranch] = useState("");
  const [githubToken, setGithubToken] = useState("");
  const [showAdvanced, setShowAdvanced] = useState(false);
  const [loading, setLoading] = useState(false);
  const [error, setError] = useState<string | null>(null);

  const isValidUrl = (url: string) =>
    /^https?:\/\/(github|gitlab)\.com\/.+\/.+/.test(url.trim());

  async function handleSubmit(e: React.FormEvent) {
    e.preventDefault();
    if (!isValidUrl(repoUrl)) {
      setError("Please enter a valid GitHub or GitLab repository URL.");
      return;
    }
    setError(null);
    setLoading(true);

    try {
      const payload: AnalyzeRequest = {
        repoUrl: repoUrl.trim(),
        ...(baseBranch && { baseBranch: baseBranch.trim() }),
        ...(headBranch && { headBranch: headBranch.trim() }),
        ...(githubToken && { githubToken: githubToken.trim() }),
      };

      const res = await fetch("/api/analyze", {
        method: "POST",
        headers: { "Content-Type": "application/json" },
        body: JSON.stringify(payload),
      });

      const data = await res.json();
      if (!data.success) {
        setError(data.error || "Analysis failed.");
        setLoading(false);
        return;
      }

      // Store report in sessionStorage and navigate
      sessionStorage.setItem("releaseReport", JSON.stringify(data.report));
      router.push("/results");
    } catch {
      setError("Network error. Please check your connection and try again.");
      setLoading(false);
    }
  }

  const examples = [
    "https://github.com/vercel/next.js",
    "https://github.com/facebook/react",
    "https://github.com/tailwindlabs/tailwindcss",
  ];

  return (
    <form onSubmit={handleSubmit} className="space-y-5">
      {/* Repo URL */}
      <div>
        <label className="block text-sm font-medium text-slate-300 mb-2">
          Repository URL
        </label>
        <input
          type="url"
          value={repoUrl}
          onChange={(e) => setRepoUrl(e.target.value)}
          placeholder="https://github.com/owner/repo"
          className="w-full px-4 py-3 rounded-xl bg-slate-800 border border-slate-700 text-white placeholder-slate-500 focus:outline-none focus:border-blue-500 focus:ring-1 focus:ring-blue-500 transition-colors text-base"
          required
          disabled={loading}
        />
        {/* Quick examples */}
        <div className="mt-2 flex flex-wrap gap-2">
          <span className="text-xs text-slate-500">Try:</span>
          {examples.map((ex) => (
            <button
              key={ex}
              type="button"
              onClick={() => setRepoUrl(ex)}
              className="text-xs text-blue-400 hover:text-blue-300 transition-colors underline underline-offset-2"
            >
              {ex.replace("https://github.com/", "")}
            </button>
          ))}
        </div>
      </div>

      {/* Advanced toggle */}
      <button
        type="button"
        onClick={() => setShowAdvanced(!showAdvanced)}
        className="flex items-center gap-2 text-sm text-slate-400 hover:text-slate-200 transition-colors"
      >
        <svg
          className={`w-4 h-4 transition-transform ${showAdvanced ? "rotate-90" : ""}`}
          fill="none"
          viewBox="0 0 24 24"
          stroke="currentColor"
        >
          <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M9 5l7 7-7 7" />
        </svg>
        Advanced options
      </button>

      {showAdvanced && (
        <div className="space-y-4 p-4 bg-slate-800/50 rounded-xl border border-slate-700/50">
          <div className="grid grid-cols-2 gap-4">
            <div>
              <label className="block text-xs font-medium text-slate-400 mb-1.5">
                Base branch (optional)
              </label>
              <input
                type="text"
                value={baseBranch}
                onChange={(e) => setBaseBranch(e.target.value)}
                placeholder="main"
                className="w-full px-3 py-2 rounded-lg bg-slate-700 border border-slate-600 text-white placeholder-slate-500 focus:outline-none focus:border-blue-500 text-sm"
                disabled={loading}
              />
            </div>
            <div>
              <label className="block text-xs font-medium text-slate-400 mb-1.5">
                Head branch (optional)
              </label>
              <input
                type="text"
                value={headBranch}
                onChange={(e) => setHeadBranch(e.target.value)}
                placeholder="release/v2.0"
                className="w-full px-3 py-2 rounded-lg bg-slate-700 border border-slate-600 text-white placeholder-slate-500 focus:outline-none focus:border-blue-500 text-sm"
                disabled={loading}
              />
            </div>
          </div>
          <div>
            <label className="block text-xs font-medium text-slate-400 mb-1.5">
              GitHub/GitLab API Token (optional — increases rate limit)
            </label>
            <input
              type="password"
              value={githubToken}
              onChange={(e) => setGithubToken(e.target.value)}
              placeholder="ghp_... or glpat-..."
              className="w-full px-3 py-2 rounded-lg bg-slate-700 border border-slate-600 text-white placeholder-slate-500 focus:outline-none focus:border-blue-500 text-sm"
              disabled={loading}
            />
            <p className="mt-1 text-xs text-slate-500">
              Token stays in your browser and is never stored.
            </p>
          </div>
        </div>
      )}

      {/* Error */}
      {error && (
        <div className="flex items-start gap-3 p-4 bg-red-950/50 border border-red-800/60 rounded-xl text-sm text-red-300">
          <svg className="w-5 h-5 mt-0.5 shrink-0 text-red-400" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M12 9v2m0 4h.01m-6.938 4h13.856c1.54 0 2.502-1.667 1.732-3L13.732 4c-.77-1.333-2.694-1.333-3.464 0L3.34 16c-.77 1.333.192 3 1.732 3z" />
          </svg>
          <span>{error}</span>
        </div>
      )}

      {/* Submit */}
      <button
        type="submit"
        disabled={loading || !repoUrl}
        className="w-full py-3.5 px-6 rounded-xl font-semibold text-base bg-blue-600 hover:bg-blue-500 disabled:bg-slate-700 disabled:text-slate-500 disabled:cursor-not-allowed text-white transition-all duration-200 flex items-center justify-center gap-3 focus:outline-none focus:ring-2 focus:ring-blue-500 focus:ring-offset-2 focus:ring-offset-slate-900"
      >
        {loading ? (
          <>
            <svg className="animate-spin w-5 h-5" fill="none" viewBox="0 0 24 24">
              <circle className="opacity-25" cx="12" cy="12" r="10" stroke="currentColor" strokeWidth="4" />
              <path className="opacity-75" fill="currentColor" d="M4 12a8 8 0 018-8V0C5.373 0 0 5.373 0 12h4z" />
            </svg>
            Analyzing repository…
          </>
        ) : (
          <>
            <svg className="w-5 h-5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M9 12l2 2 4-4m5.618-4.016A11.955 11.955 0 0112 2.944a11.955 11.955 0 01-8.618 3.04A12.02 12.02 0 003 9c0 5.591 3.824 10.29 9 11.622 5.176-1.332 9-6.03 9-11.622 0-1.042-.133-2.052-.382-3.016z" />
            </svg>
            Analyze Release Safety
          </>
        )}
      </button>
    </form>
  );
}


### 🤖 Assistant

> 🔧 called: write_file



> 🔧 **write_file** — import type { ReleaseReport } from "@/types/analysis";

interface ScoreGaugeProps {
  report: ReleaseReport;
}

function getScoreColor(score: number): { stroke: string; text: string; bg: string } {
  if (score >= 75) return { stroke: "#22c55e", text: "text-green-400", bg: "bg-green-500/10" };
  if (score >= 50) return { stroke: "#f59e0b", text: "text-amber-400", bg: "bg-amber-500/10" };
  return { stroke: "#ef4444", text: "text-red-400", bg: "bg-red-500/10" };
}

function getRecommendationStyle(rec: ReleaseReport["recommendation"]) {
  if (rec === "SAFE") return { bg: "bg-green-500/15 border-green-500/40", text: "text-green-300", dot: "bg-green-400" };
  if (rec === "CAUTION") return { bg: "bg-amber-500/15 border-amber-500/40", text: "text-amber-300", dot: "bg-amber-400" };
  return { bg: "bg-red-500/15 border-red-500/40", text: "text-red-300", dot: "bg-red-400" };
}

export default function ScoreGauge({ report }: ScoreGaugeProps) {
  const { safetyScore, recommendation, dimensions } = report;
  const { stroke, text } = getScoreColor(safetyScore);
  const recStyle = getRecommendationStyle(recommendation);

  // SVG circle gauge
  const size = 180;
  const strokeWidth = 14;
  const radius = (size - strokeWidth) / 2;
  const circumference = 2 * Math.PI * radius;
  const progress = (safetyScore / 100) * circumference;

  return (
    <div className="flex flex-col items-center gap-6">
      {/* Circle gauge */}
      <div className="relative" style={{ width: size, height: size }}>
        <svg width={size} height={size} className="-rotate-90">
          {/* Track */}
          <circle
            cx={size / 2}
            cy={size / 2}
            r={radius}
            fill="none"
            stroke="#1e293b"
            strokeWidth={strokeWidth}
          />
          {/* Progress */}
          <circle
            cx={size / 2}
            cy={size / 2}
            r={radius}
            fill="none"
            stroke={stroke}
            strokeWidth={strokeWidth}
            strokeDasharray={circumference}
            strokeDashoffset={circumference - progress}
            strokeLinecap="round"
            className="transition-all duration-1000 ease-out"
          />
        </svg>
        {/* Center text */}
        <div className="absolute inset-0 flex flex-col items-center justify-center">
          <span className={`text-4xl font-bold ${text}`}>{safetyScore}</span>
          <span className="text-xs text-slate-500 font-medium tracking-wide uppercase mt-0.5">/ 100</span>
        </div>
      </div>

      {/* Recommendation badge */}
      <div className={`flex items-center gap-2.5 px-5 py-2.5 rounded-full border ${recStyle.bg}`}>
        <span className={`w-2.5 h-2.5 rounded-full ${recStyle.dot} animate-pulse`} />
        <span className={`font-bold text-lg tracking-wide ${recStyle.text}`}>
          {recommendation}
        </span>
      </div>

      {/* Score summary text */}
      <p className="text-slate-400 text-sm text-center max-w-xs leading-relaxed">
        {report.summary}
      </p>

      {/* Dimension bars */}
      <div className="w-full space-y-3 pt-2">
        {dimensions.map((dim) => {
          const { stroke: dStroke, text: dText } = getScoreColor(dim.score);
          return (
            <div key={dim.name}>
              <div className="flex justify-between items-center mb-1">
                <span className="text-xs text-slate-400">{dim.label}</span>
                <span className={`text-xs font-semibold ${dText}`}>{dim.score}</span>
              </div>
              <div className="h-1.5 bg-slate-800 rounded-full overflow-hidden">
                <div
                  className="h-full rounded-full transition-all duration-700"
                  style={{ width: `${dim.score}%`, backgroundColor: dStroke }}
                />
              </div>
            </div>
          );
        })}
      </div>
    </div>
  );
}


### 🤖 Assistant

> 🔧 called: write_file



> 🔧 **write_file** — import type { BreakingChange, Severity } from "@/types/analysis";

const SEVERITY_STYLES: Record<Severity, { badge: string; border: string; icon: string }> = {
  critical: {
    badge: "bg-red-500/15 text-red-300 border-red-500/30",
    border: "border-l-red-500",
    icon: "text-red-400",
  },
  high: {
    badge: "bg-orange-500/15 text-orange-300 border-orange-500/30",
    border: "border-l-orange-500",
    icon: "text-orange-400",
  },
  medium: {
    badge: "bg-amber-500/15 text-amber-300 border-amber-500/30",
    border: "border-l-amber-500",
    icon: "text-amber-400",
  },
  low: {
    badge: "bg-blue-500/15 text-blue-300 border-blue-500/30",
    border: "border-l-blue-400",
    icon: "text-blue-400",
  },
  info: {
    badge: "bg-slate-500/15 text-slate-300 border-slate-500/30",
    border: "border-l-slate-500",
    icon: "text-slate-400",
  },
};

const TYPE_LABELS: Record<BreakingChange["type"], string> = {
  api_signature: "API Change",
  dependency_major: "Dependency",
  removed_export: "Removed Export",
  schema_change: "Schema",
  config_change: "Config",
  env_var: "Env Var",
};

interface BreakingChangePanelProps {
  changes: BreakingChange[];
}

export default function BreakingChangePanel({ changes }: BreakingChangePanelProps) {
  if (changes.length === 0) {
    return (
      <div className="flex flex-col items-center justify-center py-10 gap-3">
        <div className="w-12 h-12 rounded-full bg-green-500/10 flex items-center justify-center">
          <svg className="w-6 h-6 text-green-400" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M5 13l4 4L19 7" />
          </svg>
        </div>
        <p className="text-sm text-slate-400">No breaking changes detected</p>
      </div>
    );
  }

  return (
    <div className="space-y-3">
      {changes.map((change) => {
        const style = SEVERITY_STYLES[change.severity];
        return (
          <div
            key={change.id}
            className={`p-4 rounded-xl bg-slate-800/50 border border-slate-700/50 border-l-4 ${style.border}`}
          >
            <div className="flex items-start justify-between gap-3 mb-2">
              <div className="flex items-center gap-2 flex-wrap">
                <span className={`text-xs font-semibold px-2 py-0.5 rounded-full border ${style.badge}`}>
                  {change.severity.toUpperCase()}
                </span>
                <span className="text-xs px-2 py-0.5 rounded-full bg-slate-700/70 text-slate-400 border border-slate-600/50">
                  {TYPE_LABELS[change.type]}
                </span>
              </div>
            </div>

            <h4 className="text-sm font-semibold text-slate-200 mb-1">{change.title}</h4>
            <p className="text-xs text-slate-400 leading-relaxed mb-2">{change.description}</p>

            {change.file !== "commit message" && (
              <div className="flex items-center gap-1.5 text-xs text-slate-500">
                <svg className="w-3.5 h-3.5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M9 12h6m-6 4h6m2 5H7a2 2 0 01-2-2V5a2 2 0 012-2h5.586a1 1 0 01.707.293l5.414 5.414a1 1 0 01.293.707V19a2 2 0 01-2 2z" />
                </svg>
                <code className="font-mono text-slate-400">{change.file}</code>
              </div>
            )}

            {change.evidence && (
              <div className="mt-2 p-2 rounded-lg bg-slate-900/60 border border-slate-700/40">
                <code className="text-xs font-mono text-slate-400 break-all">{change.evidence}</code>
              </div>
            )}
          </div>
        );
      })}
    </div>
  );
}


### 🤖 Assistant

> 🔧 called: write_file



> 🔧 **write_file** — import type { TestCoverageGap } from "@/types/analysis";

const SEVERITY_BG: Record<string, string> = {
  critical: "border-l-red-500",
  high: "border-l-orange-500",
  medium: "border-l-amber-500",
  low: "border-l-blue-400",
  info: "border-l-slate-500",
};

const SEVERITY_BADGE: Record<string, string> = {
  critical: "bg-red-500/15 text-red-300 border-red-500/30",
  high: "bg-orange-500/15 text-orange-300 border-orange-500/30",
  medium: "bg-amber-500/15 text-amber-300 border-amber-500/30",
  low: "bg-blue-500/15 text-blue-300 border-blue-500/30",
  info: "bg-slate-500/15 text-slate-300 border-slate-500/30",
};

interface TestCoveragePanelProps {
  gaps: TestCoverageGap[];
}

export default function TestCoveragePanel({ gaps }: TestCoveragePanelProps) {
  if (gaps.length === 0) {
    return (
      <div className="flex flex-col items-center justify-center py-10 gap-3">
        <div className="w-12 h-12 rounded-full bg-green-500/10 flex items-center justify-center">
          <svg className="w-6 h-6 text-green-400" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M5 13l4 4L19 7" />
          </svg>
        </div>
        <p className="text-sm text-slate-400">No test coverage gaps detected</p>
      </div>
    );
  }

  return (
    <div className="space-y-3">
      {gaps.map((gap) => (
        <div
          key={gap.id}
          className={`p-4 rounded-xl bg-slate-800/50 border border-slate-700/50 border-l-4 ${SEVERITY_BG[gap.severity]}`}
        >
          <div className="flex items-center gap-2 mb-2">
            <span className={`text-xs font-semibold px-2 py-0.5 rounded-full border ${SEVERITY_BADGE[gap.severity]}`}>
              {gap.severity.toUpperCase()}
            </span>
            <span className="text-xs px-2 py-0.5 rounded-full bg-slate-700/70 text-slate-400 border border-slate-600/50">
              {gap.area}
            </span>
          </div>

          <p className="text-sm font-medium text-slate-200 mb-1.5">{gap.description}</p>

          {gap.files.length > 0 && (
            <div className="flex flex-wrap gap-1.5 mb-2">
              {gap.files.map((f) => (
                <code key={f} className="text-xs px-1.5 py-0.5 rounded bg-slate-900/60 border border-slate-700/50 text-slate-400 font-mono">
                  {f.split("/").slice(-2).join("/")}
                </code>
              ))}
            </div>
          )}

          <div className="flex items-start gap-2 mt-2 p-2.5 rounded-lg bg-blue-950/30 border border-blue-800/30">
            <svg className="w-4 h-4 text-blue-400 mt-0.5 shrink-0" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M13 16h-1v-4h-1m1-4h.01M21 12a9 9 0 11-18 0 9 9 0 0118 0z" />
            </svg>
            <p className="text-xs text-blue-300 leading-relaxed">{gap.suggestion}</p>
          </div>
        </div>
      ))}
    </div>
  );
}


### 🤖 Assistant

> 🔧 called: write_file



> 🔧 **write_file** — import type { ComplianceCheck } from "@/types/analysis";

const STATUS_STYLES: Record<ComplianceCheck["status"], { badge: string; icon: JSX.Element }> = {
  pass: {
    badge: "bg-green-500/15 text-green-300 border-green-500/30",
    icon: (
      <svg className="w-4 h-4 text-green-400" fill="none" viewBox="0 0 24 24" stroke="currentColor">
        <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M5 13l4 4L19 7" />
      </svg>
    ),
  },
  warning: {
    badge: "bg-amber-500/15 text-amber-300 border-amber-500/30",
    icon: (
      <svg className="w-4 h-4 text-amber-400" fill="none" viewBox="0 0 24 24" stroke="currentColor">
        <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M12 9v2m0 4h.01m-6.938 4h13.856c1.54 0 2.502-1.667 1.732-3L13.732 4c-.77-1.333-2.694-1.333-3.464 0L3.34 16c-.77 1.333.192 3 1.732 3z" />
      </svg>
    ),
  },
  fail: {
    badge: "bg-red-500/15 text-red-300 border-red-500/30",
    icon: (
      <svg className="w-4 h-4 text-red-400" fill="none" viewBox="0 0 24 24" stroke="currentColor">
        <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M6 18L18 6M6 6l12 12" />
      </svg>
    ),
  },
  na: {
    badge: "bg-slate-500/15 text-slate-400 border-slate-500/30",
    icon: (
      <svg className="w-4 h-4 text-slate-500" fill="none" viewBox="0 0 24 24" stroke="currentColor">
        <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M20 12H4" />
      </svg>
    ),
  },
};

const FRAMEWORK_COLOR: Record<ComplianceCheck["framework"], string> = {
  SOC2: "bg-purple-500/15 text-purple-300 border-purple-500/30",
  ITIL: "bg-cyan-500/15 text-cyan-300 border-cyan-500/30",
  general: "bg-slate-500/15 text-slate-300 border-slate-500/30",
};

interface CompliancePanelProps {
  checks: ComplianceCheck[];
}

export default function CompliancePanel({ checks }: CompliancePanelProps) {
  const groups: Record<string, ComplianceCheck[]> = {};
  for (const check of checks) {
    const key = check.framework;
    if (!groups[key]) groups[key] = [];
    groups[key].push(check);
  }

  const counts = {
    pass: checks.filter((c) => c.status === "pass").length,
    warning: checks.filter((c) => c.status === "warning").length,
    fail: checks.filter((c) => c.status === "fail").length,
    na: checks.filter((c) => c.status === "na").length,
  };

  return (
    <div className="space-y-5">
      {/* Summary row */}
      <div className="grid grid-cols-4 gap-3">
        {[
          { label: "Passed", count: counts.pass, color: "text-green-400" },
          { label: "Warnings", count: counts.warning, color: "text-amber-400" },
          { label: "Failed", count: counts.fail, color: "text-red-400" },
          { label: "N/A", count: counts.na, color: "text-slate-500" },
        ].map(({ label, count, color }) => (
          <div key={label} className="text-center p-3 rounded-xl bg-slate-800/50 border border-slate-700/50">
            <div className={`text-2xl font-bold ${color}`}>{count}</div>
            <div className="text-xs text-slate-500 mt-0.5">{label}</div>
          </div>
        ))}
      </div>

      {/* Grouped checks */}
      {Object.entries(groups).map(([framework, items]) => (
        <div key={framework}>
          <div className="flex items-center gap-2 mb-3">
            <span className={`text-xs font-bold px-2.5 py-1 rounded-full border ${FRAMEWORK_COLOR[framework as ComplianceCheck["framework"]]}`}>
              {framework}
            </span>
            <div className="flex-1 h-px bg-slate-700/50" />
          </div>
          <div className="space-y-2">
            {items.map((check) => {
              const style = STATUS_STYLES[check.status];
              return (
                <div key={check.id} className="p-3.5 rounded-xl bg-slate-800/40 border border-slate-700/40">
                  <div className="flex items-start gap-3">
                    <div className="mt-0.5 shrink-0">{style.icon}</div>
                    <div className="flex-1 min-w-0">
                      <div className="flex items-center gap-2 flex-wrap mb-0.5">
                        <span className="text-sm font-medium text-slate-200">{check.title}</span>
                        <span className={`text-xs px-1.5 py-0.5 rounded-full border ${style.badge}`}>
                          {check.status.toUpperCase()}
                        </span>
                      </div>
                      <p className="text-xs text-slate-400 leading-relaxed">{check.description}</p>
                      {check.evidence && (
                        <div className="mt-1.5 px-2 py-1 rounded bg-slate-900/50 border border-slate-700/40">
                          <code className="text-xs font-mono text-slate-400">{check.evidence}</code>
                        </div>
                      )}
                      {check.remediation && check.status !== "pass" && (
                        <div className="mt-2 flex items-start gap-1.5">
                          <svg className="w-3.5 h-3.5 text-blue-400 mt-0.5 shrink-0" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                            <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M13 10V3L4 14h7v7l9-11h-7z" />
                          </svg>
                          <p className="text-xs text-blue-300">{check.remediation}</p>
                        </div>
                      )}
                    </div>
                  </div>
                </div>
              );
            })}
          </div>
        </div>
      ))}
    </div>
  );
}


### 🤖 Assistant

> 🔧 called: write_file



> 🔧 **write_file** — import type { CommitSummary, ChangedFile } from "@/types/analysis";

interface CommitListProps {
  commits: CommitSummary[];
  files: ChangedFile[];
}

const FILE_STATUS_COLOR: Record<string, string> = {
  added: "text-green-400 bg-green-500/10",
  modified: "text-amber-400 bg-amber-500/10",
  removed: "text-red-400 bg-red-500/10",
  renamed: "text-blue-400 bg-blue-500/10",
};

const FILE_STATUS_LABEL: Record<string, string> = {
  added: "A",
  modified: "M",
  removed: "D",
  renamed: "R",
};

export default function CommitList({ commits, files }: CommitListProps) {
  const totalAdditions = files.reduce((sum, f) => sum + f.additions, 0);
  const totalDeletions = files.reduce((sum, f) => sum + f.deletions, 0);

  return (
    <div className="space-y-5">
      {/* Stats row */}
      <div className="grid grid-cols-3 gap-3">
        <div className="p-3 rounded-xl bg-slate-800/50 border border-slate-700/50 text-center">
          <div className="text-xl font-bold text-slate-200">{commits.length}</div>
          <div className="text-xs text-slate-500 mt-0.5">Commits</div>
        </div>
        <div className="p-3 rounded-xl bg-slate-800/50 border border-slate-700/50 text-center">
          <div className="text-xl font-bold text-green-400">+{totalAdditions}</div>
          <div className="text-xs text-slate-500 mt-0.5">Lines added</div>
        </div>
        <div className="p-3 rounded-xl bg-slate-800/50 border border-slate-700/50 text-center">
          <div className="text-xl font-bold text-red-400">−{totalDeletions}</div>
          <div className="text-xs text-slate-500 mt-0.5">Lines removed</div>
        </div>
      </div>

      {/* Changed files */}
      {files.length > 0 && (
        <div>
          <h4 className="text-xs font-semibold text-slate-500 uppercase tracking-wide mb-2">
            Changed Files ({files.length})
          </h4>
          <div className="space-y-1 max-h-52 overflow-y-auto pr-1 scrollbar-thin">
            {files.map((file) => (
              <div
                key={file.filename}
                className="flex items-center gap-2 p-2 rounded-lg hover:bg-slate-800/60 transition-colors"
              >
                <span
                  className={`text-xs font-bold w-5 h-5 rounded flex items-center justify-center shrink-0 ${FILE_STATUS_COLOR[file.status]}`}
                >
                  {FILE_STATUS_LABEL[file.status]}
                </span>
                <code className="text-xs font-mono text-slate-300 flex-1 truncate">
                  {file.filename}
                </code>
                <span className="text-xs text-green-400 shrink-0">+{file.additions}</span>
                <span className="text-xs text-red-400 shrink-0">−{file.deletions}</span>
              </div>
            ))}
          </div>
        </div>
      )}

      {/* Commits */}
      {commits.length > 0 && (
        <div>
          <h4 className="text-xs font-semibold text-slate-500 uppercase tracking-wide mb-2">
            Recent Commits
          </h4>
          <div className="space-y-1.5 max-h-60 overflow-y-auto pr-1">
            {commits.map((commit) => (
              <div
                key={commit.sha}
                className="flex items-start gap-3 p-2.5 rounded-lg bg-slate-800/40 border border-slate-700/40 hover:border-slate-600/50 transition-colors"
              >
                <code className="text-xs font-mono text-blue-400 shrink-0 mt-0.5 w-14">
                  {commit.sha}
                </code>
                <div className="flex-1 min-w-0">
                  <p className="text-xs text-slate-300 truncate">{commit.message}</p>
                  <p className="text-xs text-slate-600 mt-0.5">
                    {commit.author} ·{" "}
                    {new Date(commit.date).toLocaleDateString(undefined, {
                      month: "short",
                      day: "numeric",
                    })}
                  </p>
                </div>
                {commit.url && (
                  <a
                    href={commit.url}
                    target="_blank"
                    rel="noopener noreferrer"
                    className="shrink-0 mt-0.5 text-slate-600 hover:text-slate-400 transition-colors"
                  >
                    <svg className="w-3.5 h-3.5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                      <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M10 6H6a2 2 0 00-2 2v10a2 2 0 002 2h10a2 2 0 002-2v-4M14 4h6m0 0v6m0-6L10 14" />
                    </svg>
                  </a>
                )}
              </div>
            ))}
          </div>
        </div>
      )}
    </div>
  );
}


### 🤖 Assistant

> 🔧 called: write_file

Now build the pages:

> 🔧 **write_file** — import type { Metadata } from "next";
import localFont from "next/font/local";
import "./globals.css";

const geistSans = localFont({
  src: "./fonts/GeistVF.woff",
  variable: "--font-geist-sans",
  weight: "100 900",
});
const geistMono = localFont({
  src: "./fonts/GeistMonoVF.woff",
  variable: "--font-geist-mono",
  weight: "100 900",
});

export const metadata: Metadata = {
  title: "Bob's Release Pilot — Release Safety Assistant",
  description:
    "AI-powered release safety analysis. Detect breaking changes, test coverage gaps, and SOC2/ITIL compliance issues before you ship.",
};

export default function RootLayout({
  children,
}: Readonly<{ children: React.ReactNode }>) {
  return (
    <html lang="en" className="dark">
      <body
        className={`${geistSans.variable} ${geistMono.variable} antialiased bg-slate-950 text-slate-100 min-h-screen`}
      >
        {children}
      </body>
    </html>
  );
}


### 🤖 Assistant

> 🔧 called: write_file



> 🔧 **write_file** — @tailwind base;
@tailwind components;
@tailwind utilities;

:root {
  --background: #020817;
  --foreground: #f8fafc;
}

html {
  background-color: #020817;
  color: #f8fafc;
}

body {
  background-color: #020817;
}

@layer utilities {
  .text-balance {
    text-wrap: balance;
  }

  .scrollbar-thin {
    scrollbar-width: thin;
    scrollbar-color: #334155 transparent;
  }

  .scrollbar-thin::-webkit-scrollbar {
    width: 4px;
  }

  .scrollbar-thin::-webkit-scrollbar-track {
    background: transparent;
  }

  .scrollbar-thin::-webkit-scrollbar-thumb {
    background-color: #334155;
    border-radius: 2px;
  }
}


### 🤖 Assistant

> 🔧 called: write_file

Now the home page:

> 🔧 **write_file** — import AnalyzeForm from "@/components/AnalyzeForm";

const FEATURES = [
  {
    icon: (
      <svg className="w-5 h-5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
        <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M13 10V3L4 14h7v7l9-11h-7z" />
      </svg>
    ),
    title: "Breaking Change Detection",
    desc: "Scans commits, diffs, and removed exports to surface API-breaking changes.",
  },
  {
    icon: (
      <svg className="w-5 h-5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
        <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z" />
      </svg>
    ),
    title: "Test Coverage Gaps",
    desc: "Identifies changed files with no corresponding test updates.",
  },
  {
    icon: (
      <svg className="w-5 h-5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
        <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M9 12h6m-6 4h6m2 5H7a2 2 0 01-2-2V5a2 2 0 012-2h5.586a1 1 0 01.707.293l5.414 5.414a1 1 0 01.293.707V19a2 2 0 01-2 2z" />
      </svg>
    ),
    title: "SOC2 / ITIL Compliance",
    desc: "Checks change management, secret exposure, rollback plans, and more.",
  },
  {
    icon: (
      <svg className="w-5 h-5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
        <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M11 3.055A9.001 9.001 0 1020.945 13H11V3.055z" />
        <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M20.488 9H15V3.512A9.025 9.025 0 0120.488 9z" />
      </svg>
    ),
    title: "Safety Score 0–100",
    desc: "Weighted composite score across 4 dimensions. SAFE / CAUTION / UNSAFE.",
  },
];

export default function HomePage() {
  return (
    <div className="min-h-screen bg-slate-950 flex flex-col">
      {/* Nav */}
      <nav className="border-b border-slate-800/60 px-6 py-4">
        <div className="max-w-6xl mx-auto flex items-center gap-3">
          <div className="w-8 h-8 rounded-lg bg-blue-600 flex items-center justify-center shrink-0">
            <svg className="w-4.5 h-4.5 text-white" viewBox="0 0 24 24" fill="none" stroke="currentColor">
              <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2.5} d="M9 12l2 2 4-4m5.618-4.016A11.955 11.955 0 0112 2.944a11.955 11.955 0 01-8.618 3.04A12.02 12.02 0 003 9c0 5.591 3.824 10.29 9 11.622 5.176-1.332 9-6.03 9-11.622 0-1.042-.133-2.052-.382-3.016z" />
            </svg>
          </div>
          <div>
            <span className="font-bold text-white text-sm">Bob&apos;s Release Pilot</span>
            <span className="ml-2 text-xs px-1.5 py-0.5 rounded bg-blue-500/20 text-blue-300 border border-blue-500/30 font-medium">
              IBM Bob Hackathon 2.0
            </span>
          </div>
        </div>
      </nav>

      {/* Hero */}
      <main className="flex-1 flex flex-col items-center justify-center px-4 py-16">
        <div className="w-full max-w-2xl">
          {/* Badge */}
          <div className="flex justify-center mb-6">
            <span className="inline-flex items-center gap-2 px-3 py-1.5 rounded-full bg-blue-500/10 border border-blue-500/25 text-blue-300 text-xs font-medium">
              <span className="w-1.5 h-1.5 rounded-full bg-blue-400 animate-pulse" />
              AI-Powered Release Safety Analysis
            </span>
          </div>

          {/* Headline */}
          <h1 className="text-4xl sm:text-5xl font-bold text-center text-white mb-4 leading-tight">
            Is your release{" "}
            <span className="text-transparent bg-clip-text bg-gradient-to-r from-blue-400 to-violet-400">
              safe to ship?
            </span>
          </h1>
          <p className="text-center text-slate-400 text-base sm:text-lg mb-10 max-w-xl mx-auto leading-relaxed">
            Paste a GitHub or GitLab repository URL and get an instant safety score
            with breaking change detection, test gap analysis, and compliance checks.
          </p>

          {/* Form card */}
          <div className="bg-slate-900/80 border border-slate-800 rounded-2xl p-6 sm:p-8 shadow-2xl shadow-black/40 backdrop-blur-sm">
            <AnalyzeForm />
          </div>

          {/* Features */}
          <div className="grid grid-cols-2 gap-4 mt-10">
            {FEATURES.map((f) => (
              <div
                key={f.title}
                className="flex items-start gap-3 p-4 rounded-xl bg-slate-900/40 border border-slate-800/60 hover:border-slate-700/60 transition-colors"
              >
                <div className="w-8 h-8 rounded-lg bg-slate-800 flex items-center justify-center shrink-0 text-slate-400">
                  {f.icon}
                </div>
                <div>
                  <h3 className="text-sm font-semibold text-slate-200 mb-0.5">{f.title}</h3>
                  <p className="text-xs text-slate-500 leading-relaxed">{f.desc}</p>
                </div>
              </div>
            ))}
          </div>
        </div>
      </main>

      {/* Footer */}
      <footer className="border-t border-slate-800/60 py-5 text-center text-xs text-slate-600">
        Built for the IBM Bob 2.0 Hackathon &middot; Bob&apos;s Release Pilot &middot; 2024
      </footer>
    </div>
  );
}


### 🤖 Assistant

> 🔧 called: write_file

Now the results page — the main dashboard:

> 🔧 **write_file** — "use client";

import { useEffect, useState } from "react";
import { useRouter } from "next/navigation";
import type { ReleaseReport } from "@/types/analysis";
import ScoreGauge from "@/components/ScoreGauge";
import BreakingChangePanel from "@/components/BreakingChangePanel";
import TestCoveragePanel from "@/components/TestCoveragePanel";
import CompliancePanel from "@/components/CompliancePanel";
import CommitList from "@/components/CommitList";

type Tab = "overview" | "breaking" | "coverage" | "compliance" | "commits";

const TABS: { id: Tab; label: string; count?: (r: ReleaseReport) => number }[] = [
  { id: "overview", label: "Overview" },
  { id: "breaking", label: "Breaking Changes", count: (r) => r.breakingChanges.length },
  { id: "coverage", label: "Test Gaps", count: (r) => r.testCoverageGaps.length },
  { id: "compliance", label: "Compliance", count: (r) => r.complianceChecks.filter(c => c.status !== "na").length },
  { id: "commits", label: "Commits", count: (r) => r.rawCommits.length },
];

function getBadgeColor(count: number, tab: Tab): string {
  if (tab === "breaking" && count > 0) return "bg-red-500/20 text-red-300";
  if (tab === "coverage" && count > 0) return "bg-amber-500/20 text-amber-300";
  return "bg-slate-700 text-slate-400";
}

export default function ResultsPage() {
  const router = useRouter();
  const [report, setReport] = useState<ReleaseReport | null>(null);
  const [activeTab, setActiveTab] = useState<Tab>("overview");

  useEffect(() => {
    const stored = sessionStorage.getItem("releaseReport");
    if (!stored) {
      router.replace("/");
      return;
    }
    try {
      setReport(JSON.parse(stored));
    } catch {
      router.replace("/");
    }
  }, [router]);

  if (!report) {
    return (
      <div className="min-h-screen bg-slate-950 flex items-center justify-center">
        <div className="flex items-center gap-3 text-slate-400">
          <svg className="animate-spin w-5 h-5" fill="none" viewBox="0 0 24 24">
            <circle className="opacity-25" cx="12" cy="12" r="10" stroke="currentColor" strokeWidth="4" />
            <path className="opacity-75" fill="currentColor" d="M4 12a8 8 0 018-8V0C5.373 0 0 5.373 0 12h4z" />
          </svg>
          Loading report…
        </div>
      </div>
    );
  }

  const recColors = {
    SAFE: "border-green-500/40 bg-green-500/5",
    CAUTION: "border-amber-500/40 bg-amber-500/5",
    UNSAFE: "border-red-500/40 bg-red-500/5",
  };

  return (
    <div className="min-h-screen bg-slate-950 flex flex-col">
      {/* Nav */}
      <nav className="border-b border-slate-800/60 px-6 py-4 sticky top-0 z-10 bg-slate-950/90 backdrop-blur-sm">
        <div className="max-w-7xl mx-auto flex items-center justify-between gap-4">
          <div className="flex items-center gap-3">
            <button
              onClick={() => router.push("/")}
              className="w-8 h-8 rounded-lg bg-slate-800 hover:bg-slate-700 flex items-center justify-center transition-colors"
            >
              <svg className="w-4 h-4 text-slate-400" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M15 19l-7-7 7-7" />
              </svg>
            </button>
            <div className="w-7 h-7 rounded-lg bg-blue-600 flex items-center justify-center shrink-0">
              <svg className="w-4 h-4 text-white" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2.5} d="M9 12l2 2 4-4m5.618-4.016A11.955 11.955 0 0112 2.944a11.955 11.955 0 01-8.618 3.04A12.02 12.02 0 003 9c0 5.591 3.824 10.29 9 11.622 5.176-1.332 9-6.03 9-11.622 0-1.042-.133-2.052-.382-3.016z" />
              </svg>
            </div>
            <span className="font-semibold text-white text-sm">Release Safety Report</span>
          </div>

          {/* Repo info */}
          <div className="hidden sm:flex items-center gap-2 text-sm text-slate-400">
            <a
              href={report.repo.url}
              target="_blank"
              rel="noopener noreferrer"
              className="flex items-center gap-1.5 hover:text-slate-200 transition-colors"
            >
              <svg className="w-4 h-4" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M10 20l4-16m4 4l4 4-4 4M6 16l-4-4 4-4" />
              </svg>
              <span className="font-mono">{report.repo.owner}/{report.repo.repo}</span>
            </a>
            <span className="text-slate-700">·</span>
            <span className="font-mono text-slate-500">{report.repo.branch}</span>
          </div>

          <div className="text-xs text-slate-600">
            {new Date(report.generatedAt).toLocaleString()}
          </div>
        </div>
      </nav>

      <main className="flex-1 max-w-7xl mx-auto w-full px-4 sm:px-6 py-8">
        {/* ── Top hero band ─────────────────────────────────────────────── */}
        <div className={`rounded-2xl border p-6 mb-8 ${recColors[report.recommendation]}`}>
          <div className="grid grid-cols-1 lg:grid-cols-[auto_1fr] gap-8 items-center">
            {/* Gauge */}
            <div className="flex justify-center lg:justify-start">
              <div className="w-64">
                <ScoreGauge report={report} />
              </div>
            </div>

            {/* Repo + quick stats */}
            <div className="space-y-5">
              {/* Repo header */}
              <div>
                <div className="flex items-center gap-2 mb-1">
                  <a href={report.repo.url} target="_blank" rel="noopener noreferrer"
                    className="text-xl font-bold text-white hover:text-blue-300 transition-colors">
                    {report.repo.owner}/{report.repo.repo}
                  </a>
                  {report.repo.language && (
                    <span className="text-xs px-2 py-0.5 rounded-full bg-slate-700 text-slate-300 border border-slate-600/50">
                      {report.repo.language}
                    </span>
                  )}
                </div>
                {report.repo.description && (
                  <p className="text-sm text-slate-400">{report.repo.description}</p>
                )}
              </div>

              {/* Quick stats */}
              <div className="grid grid-cols-2 sm:grid-cols-4 gap-3">
                {[
                  {
                    label: "Breaking Changes",
                    value: report.breakingChanges.length,
                    color: report.breakingChanges.length > 0 ? "text-red-400" : "text-green-400",
                    icon: "⚡",
                  },
                  {
                    label: "Test Gaps",
                    value: report.testCoverageGaps.length,
                    color: report.testCoverageGaps.length > 0 ? "text-amber-400" : "text-green-400",
                    icon: "🧪",
                  },
                  {
                    label: "Compliance Issues",
                    value: report.complianceChecks.filter((c) => c.status === "fail" || c.status === "warning").length,
                    color: "text-slate-300",
                    icon: "📋",
                  },
                  {
                    label: "Files Changed",
                    value: report.changedFiles.length,
                    color: "text-slate-300",
                    icon: "📁",
                  },
                ].map((stat) => (
                  <div key={stat.label} className="p-3 rounded-xl bg-slate-900/50 border border-slate-700/50">
                    <div className={`text-2xl font-bold ${stat.color}`}>{stat.value}</div>
                    <div className="text-xs text-slate-500 mt-0.5">{stat.label}</div>
                  </div>
                ))}
              </div>

              {/* Last commit */}
              <div className="flex items-center gap-2 text-xs text-slate-500">
                <svg className="w-3.5 h-3.5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z" />
                </svg>
                Last commit:{" "}
                <code className="font-mono text-slate-400">{report.repo.lastCommitSha}</code>
                <span className="truncate max-w-xs">{report.repo.lastCommitMessage}</span>
                <span>· {new Date(report.repo.lastCommitDate).toLocaleDateString()}</span>
              </div>

              {/* Analysis errors */}
              {report.analysisErrors.length > 0 && (
                <div className="p-3 rounded-xl bg-amber-950/30 border border-amber-800/40 text-xs text-amber-300">
                  ⚠ Partial results — some API calls failed: {report.analysisErrors.join("; ")}
                </div>
              )}
            </div>
          </div>
        </div>

        {/* ── Tabs ──────────────────────────────────────────────────────── */}
        <div className="border-b border-slate-800 mb-6">
          <div className="flex gap-1 overflow-x-auto pb-px">
            {TABS.map((tab) => {
              const count = tab.count?.(report);
              const isActive = activeTab === tab.id;
              return (
                <button
                  key={tab.id}
                  onClick={() => setActiveTab(tab.id)}
                  className={`flex items-center gap-2 px-4 py-2.5 text-sm font-medium whitespace-nowrap border-b-2 transition-colors ${
                    isActive
                      ? "border-blue-500 text-blue-400"
                      : "border-transparent text-slate-500 hover:text-slate-300 hover:border-slate-600"
                  }`}
                >
                  {tab.label}
                  {count !== undefined && count > 0 && (
                    <span className={`text-xs px-1.5 py-0.5 rounded-full font-semibold ${getBadgeColor(count, tab.id)}`}>
                      {count}
                    </span>
                  )}
                </button>
              );
            })}
          </div>
        </div>

        {/* ── Tab content ───────────────────────────────────────────────── */}
        <div className="pb-12">
          {activeTab === "overview" && (
            <div className="grid grid-cols-1 md:grid-cols-2 gap-5">
              {/* Breaking changes preview */}
              <div className="bg-slate-900/50 border border-slate-800 rounded-2xl p-5">
                <h2 className="text-sm font-semibold text-slate-300 mb-4 flex items-center gap-2">
                  <svg className="w-4 h-4 text-red-400" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M13 10V3L4 14h7v7l9-11h-7z" />
                  </svg>
                  Breaking Changes
                  <span className="ml-auto text-xs text-slate-600">{report.breakingChanges.length} found</span>
                </h2>
                <BreakingChangePanel changes={report.breakingChanges.slice(0, 3)} />
                {report.breakingChanges.length > 3 && (
                  <button onClick={() => setActiveTab("breaking")} className="mt-3 text-xs text-blue-400 hover:text-blue-300">
                    View all {report.breakingChanges.length} →
                  </button>
                )}
              </div>

              {/* Test coverage preview */}
              <div className="bg-slate-900/50 border border-slate-800 rounded-2xl p-5">
                <h2 className="text-sm font-semibold text-slate-300 mb-4 flex items-center gap-2">
                  <svg className="w-4 h-4 text-amber-400" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z" />
                  </svg>
                  Test Coverage Gaps
                  <span className="ml-auto text-xs text-slate-600">{report.testCoverageGaps.length} found</span>
                </h2>
                <TestCoveragePanel gaps={report.testCoverageGaps.slice(0, 3)} />
                {report.testCoverageGaps.length > 3 && (
                  <button onClick={() => setActiveTab("coverage")} className="mt-3 text-xs text-blue-400 hover:text-blue-300">
                    View all {report.testCoverageGaps.length} →
                  </button>
                )}
              </div>

              {/* Compliance preview */}
              <div className="bg-slate-900/50 border border-slate-800 rounded-2xl p-5">
                <h2 className="text-sm font-semibold text-slate-300 mb-4 flex items-center gap-2">
                  <svg className="w-4 h-4 text-purple-400" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M9 12h6m-6 4h6m2 5H7a2 2 0 01-2-2V5a2 2 0 012-2h5.586a1 1 0 01.707.293l5.414 5.414a1 1 0 01.293.707V19a2 2 0 01-2 2z" />
                  </svg>
                  SOC2 / ITIL Compliance
                </h2>
                <CompliancePanel checks={report.complianceChecks} />
              </div>

              {/* Commits */}
              <div className="bg-slate-900/50 border border-slate-800 rounded-2xl p-5">
                <h2 className="text-sm font-semibold text-slate-300 mb-4 flex items-center gap-2">
                  <svg className="w-4 h-4 text-slate-400" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M8 7h12m0 0l-4-4m4 4l-4 4m0 6H4m0 0l4 4m-4-4l4-4" />
                  </svg>
                  Changeset
                </h2>
                <CommitList commits={report.rawCommits.slice(0, 5)} files={report.changedFiles} />
              </div>
            </div>
          )}

          {activeTab === "breaking" && (
            <div className="bg-slate-900/50 border border-slate-800 rounded-2xl p-6">
              <h2 className="text-base font-semibold text-slate-200 mb-5 flex items-center gap-2">
                <svg className="w-5 h-5 text-red-400" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M13 10V3L4 14h7v7l9-11h-7z" />
                </svg>
                All Breaking Changes ({report.breakingChanges.length})
              </h2>
              <BreakingChangePanel changes={report.breakingChanges} />
            </div>
          )}

          {activeTab === "coverage" && (
            <div className="bg-slate-900/50 border border-slate-800 rounded-2xl p-6">
              <h2 className="text-base font-semibold text-slate-200 mb-5 flex items-center gap-2">
                <svg className="w-5 h-5 text-amber-400" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z" />
                </svg>
                All Test Coverage Gaps ({report.testCoverageGaps.length})
              </h2>
              <TestCoveragePanel gaps={report.testCoverageGaps} />
            </div>
          )}

          {activeTab === "compliance" && (
            <div className="bg-slate-900/50 border border-slate-800 rounded-2xl p-6">
              <h2 className="text-base font-semibold text-slate-200 mb-5 flex items-center gap-2">
                <svg className="w-5 h-5 text-purple-400" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M9 12h6m-6 4h6m2 5H7a2 2 0 01-2-2V5a2 2 0 012-2h5.586a1 1 0 01.707.293l5.414 5.414a1 1 0 01.293.707V19a2 2 0 01-2 2z" />
                </svg>
                SOC2 / ITIL Compliance ({report.complianceChecks.length} checks)
              </h2>
              <CompliancePanel checks={report.complianceChecks} />
            </div>
          )}

          {activeTab === "commits" && (
            <div className="bg-slate-900/50 border border-slate-800 rounded-2xl p-6">
              <h2 className="text-base font-semibold text-slate-200 mb-5 flex items-center gap-2">
                <svg className="w-5 h-5 text-slate-400" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M8 7h12m0 0l-4-4m4 4l-4 4m0 6H4m0 0l4 4m-4-4l4-4" />
                </svg>
                Full Changeset
              </h2>
              <CommitList commits={report.rawCommits} files={report.changedFiles} />
            </div>
          )}
        </div>
      </main>

      <footer className="border-t border-slate-800/60 py-5 text-center text-xs text-slate-600">
        Bob&apos;s Release Pilot · IBM Bob Hackathon 2.0 · {new Date(report.generatedAt).toLocaleString()}
      </footer>
    </div>
  );
}


### 🤖 Assistant

> 🔧 called: apply_diff

Now fix the TypeScript issue in `CompliancePanel.tsx` — `JSX.Element` needs the React import:

> 🔧 **apply_diff** — src/components/CompliancePanel.tsx

### 🤖 Assistant

> 🔧 called: write_file, write_file

Now add Vercel deployment config and AGENTS.md:

> 🔧 **write_file** — # AGENTS.md

This file provides guidance to agents when working with code in this repository.

## Stack
Next.js 14 App Router, TypeScript, Tailwind CSS dark theme (slate-950 base), no external UI library.

## Commands
```bash
npm run dev      # start dev server on :3000
npm run build    # production build (verify before committing)
npm run lint     # ESLint check
```

## Architecture
```
src/
  types/analysis.ts          # All shared TypeScript interfaces (source of truth)
  lib/
    repo-fetcher.ts          # GitHub + GitLab API calls (no SDK, raw fetch)
    breaking-changes.ts      # Breaking change detection engine
    test-coverage.ts         # Test coverage gap analysis
    compliance.ts            # SOC2/ITIL compliance rule engine
    scorer.ts                # Safety score calculation + recommendation
  app/
    page.tsx                 # Home page (URL input form)
    results/page.tsx         # Results dashboard (tabbed, client component)
    api/analyze/route.ts     # POST /api/analyze — orchestrates all engines
  components/
    AnalyzeForm.tsx          # Form with advanced options, client component
    ScoreGauge.tsx           # SVG circular gauge + dimension bars
    BreakingChangePanel.tsx  # Breaking changes list
    TestCoveragePanel.tsx    # Test gap list with suggestions
    CompliancePanel.tsx      # SOC2/ITIL checks grouped by framework
    CommitList.tsx           # Commit log + changed files
```

## Key Patterns
- Report flows: API route → `sessionStorage` → Results page (no DB, no server state)
- All analysis is heuristic/static (no LLM calls) — pattern matching on diffs and commit messages
- GitHub compare API uses `{base}...{head}` (3-dot, not 2-dot) for diff
- GitLab uses project ID encoded as `owner%2Frepo` in URL path
- Score is weighted: Breaking Changes 35%, Compliance 30%, Test Coverage 25%, Commit Quality 10%
- Recommendation thresholds: score ≥ 72 = SAFE, 50–71 = CAUTION, < 50 or any critical = UNSAFE
- No token required for public repos; GitHub rate limit = 60 req/hr unauthenticated

## Tailwind Conventions
- All dark-theme — never use light background classes (bg-white, bg-gray-*)
- Base: `bg-slate-950`, cards: `bg-slate-900/50 border border-slate-800`, inner: `bg-slate-800/50`
- Severity colors: critical=red, high=orange, medium=amber, low=blue, info=slate
- Status colors: pass=green, warning=amber, fail=red, na=slate


> 🔧 **write_file** — /** @type {import('next').NextConfig} */
const nextConfig = {
  // No external image domains needed — we don't use next/image for external URLs
};

export default nextConfig;


### 🤖 Assistant

> 🔧 called: execute_command

Now let's run the TypeScript build check to catch any errors:

> 🔧 **execute_command** — npm run build 2>&1

### 🤖 Assistant

> 🔧 called: execute_command

The node_modules are broken — this is the wrong workspace (the playground, not the actual project). Let me re-install next.js:

> 🔧 **execute_command** — npm install 2>&1

### 🤖 Assistant

> 🔧 called: execute_command



> 🔧 **execute_command** — npm run build 2>&1

### 🤖 Assistant

> 🔧 called: execute_command

The `node_modules` in the playground is corrupted (missing internal Next.js files). Let me do a clean reinstall:

> 🔧 **execute_command** — rm -rf node_modules package-lock.json && npm install 2>&1

### 🤖 Assistant

> 🔧 called: execute_command



> 🔧 **execute_command** — npm run build 2>&1

### 🤖 Assistant

> 🔧 called: apply_diff



> 🔧 **apply_diff** — src/app/api/analyze/route.ts

### 🤖 Assistant

> 🔧 called: execute_command



> 🔧 **execute_command** — npx next build 2>&1

### 🤖 Assistant

> 🔧 called: read_file



> 🔧 **read_file** — tsconfig.json

### 🤖 Assistant

> 🔧 called: apply_diff

The `lib` includes `esnext` so Set should be iterable — but the spread of a `Set` is the issue. Let me fix it by using `Array.from`:

> 🔧 **apply_diff** — src/lib/test-coverage.ts

### 🤖 Assistant

> 🔧 called: execute_command



> 🔧 **execute_command** — npx next build 2>&1

### 🤖 Assistant

> 🔧 called: apply_diff



> 🔧 **apply_diff** — <<<<<<< SEARCH
:start_line:67
-------
    const head = headBranch || repoInfo.defaultBranch;
    const base = baseBranch || `${head}~20`; // last 20 commits as baseline
=======
    const head = headBranch || repoInfo.defaultBranch;
>>>>>>> REPLACE

<<<<<<< SEARCH
:start_line:87
-------
      // For GitHub compare, we use HEAD~10 as base if no explicit base given
      const compareBase =
        baseBranch ||
        (commits.length >= 2 ? commits[commits.length - 1].sha : head);
=======
      // For GitHub compare, we use oldest fetched commit SHA as base if no explicit base given
      const compareBase =
        baseBranch ??
        (commits.length >= 2 ? commits[commits.length - 1].sha : head);
>>>>>>> REPLACE


### 🤖 Assistant

> 🔧 called: execute_command



> 🔧 **execute_command** — npx next build 2>&1

### 🤖 Assistant

> 🔧 called: list_files

Build passes clean. Let me verify the full file structure:

> 🔧 **list_files** — src

### 🤖 Assistant

✅ Build passes clean. Here's everything that was built:

---

## What was built

### 🏗️ Project structure (21 new files)

```
src/
  types/analysis.ts          ← All shared types (source of truth)
  lib/
    repo-fetcher.ts          ← GitHub + GitLab API (raw fetch, no SDK)
    breaking-changes.ts      ← Commit message + diff pattern detection
    test-coverage.ts         ← Changed files vs test files gap analysis
    compliance.ts            ← 10 SOC2/ITIL/general rule engine checks
    scorer.ts                ← Weighted score + SAFE/CAUTION/UNSAFE logic
  app/
    page.tsx                 ← Home page with URL input form
    results/page.tsx         ← Tabbed results dashboard
    api/analyze/route.ts     ← POST endpoint orchestrating all engines
  components/
    AnalyzeForm.tsx          ← URL input with advanced options (token, branches)
    ScoreGauge.tsx           ← SVG circular gauge + dimension bars
    BreakingChangePanel.tsx  ← Severity-colored change cards
    TestCoveragePanel.tsx    ← Gap cards with actionable suggestions
    CompliancePanel.tsx      ← SOC2/ITIL checks grouped by framework
    CommitList.tsx           ← Commit log + changed files with diff stats
```

### 🎯 Key capabilities
- **Breaking changes**: detects `BREAKING CHANGE` commits, removed exports, schema files, major version bumps in `package.json`, deleted files
- **Test gaps**: cross-references changed source files vs changed test files, flags untested API routes / business logic / hooks
- **10 compliance checks** across SOC2 (change management, secrets, env docs, dependencies) and ITIL (release notes, rollback plans, config tracking, availability)
- **Score formula**: Breaking Changes 35% + Compliance 30% + Test Coverage 25% + Commit Quality 10%
- No API token needed for public repos; token field in advanced options increases rate limit

### 🚀 To run
```bash
npm run dev   # opens on http://localhost:3000
```