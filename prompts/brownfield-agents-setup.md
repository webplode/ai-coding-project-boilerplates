# Prompt: Generate AGENTS.md for a Brownfield (Existing) Project

> Copy this prompt and paste it into your AI coding agent (Claude Code, Cursor, etc.) inside an existing project. The agent will explore the codebase and fill in the AGENTS.md boilerplate automatically.

---

## The Prompt

```
I have an existing project and need you to fill in the AGENTS.md boilerplate template.
The boilerplate is located at: <path to your AGENTS.md boilerplate, or paste it inline>

**Project Name:** <your project name>

**What it does (1-3 sentences):**
<describe what the system does, who uses it, and what problem it solves>

**Key Design Decisions that aren't obvious from code:**
<list any non-obvious architectural choices — e.g., "multi-tenant with tenant ID on every entity",
"advisory locks to prevent duplicate jobs", "we never delete rows, only soft-delete",
"auth tokens are short-lived, refresh tokens in httpOnly cookies">
If none come to mind, say "discover from code".

**Build & Lint Commands:**
- Backend build: <e.g., npm run build — or say "discover from package.json / Makefile / etc.">
- Backend lint: <e.g., npm run lint — or "discover">
- Frontend build: <e.g., npm run build — or "discover" or "N/A">
- Frontend lint: <e.g., npm run lint — or "discover" or "N/A">

---

Now, do the following:

### Phase 1: Explore the Codebase

Before filling anything in, thoroughly explore the project:

1. Read the root directory structure (`ls`, manifest files like package.json / Cargo.toml / pyproject.toml / go.mod).
2. Identify the tech stack: languages, frameworks, ORMs, test runners, build tools.
3. Identify the package manager in use (check lock files: package-lock.json → npm, yarn.lock → yarn, pnpm-lock.yaml → pnpm, Cargo.lock → cargo, poetry.lock → poetry, etc.).
4. Map the directory structure — identify backend dir, frontend dir (if any), shared libs, config, docs.
5. Find the entry points (main.ts, app.py, main.go, etc.) and trace the bootstrap flow.
6. Identify core modules/domains by reading the src/ directory tree.
7. Read key files: auth modules, database config, ORM entities/models, API routes.
8. Check for queue/worker/job systems.
9. Read existing README, docs/, or architecture files for context.
10. Look at the build/lint scripts in the manifest files.

### Phase 2: Fill in the AGENTS.md

Using what you discovered:

1. Replace ALL `<placeholder>` values and `<!-- CUSTOMIZE: -->` comments with real values from the codebase.
2. **Toolchain section:** Fill in the actual runtime, framework, ORM, queue, auth, validation, and package manager. Populate the dependency tables with the project's actual core packages (not every package — just the important ones).
3. **Compiler Checks:** Fill in the actual build and lint commands you found in the manifest files.
4. **Architecture diagram:** Create an ASCII diagram that reflects the actual architecture — not a generic template. Show the real layers, protocols, and integrations.
5. **Workspace Structure:** Show the actual directory tree (depth 2-3), not a generic one.
6. **Key Files:** List the actual critical files with their real paths and accurate descriptions of what they do.
7. **Key Design Decisions:** Combine what I told you with what you discovered in the code. Focus on invariants and non-obvious choices that an agent could accidentally break.
8. Remove all `<!-- CUSTOMIZE: -->` HTML comments — the final file should read as project-specific documentation.
9. Keep ALL sections from "MCP Agent Mail" to the end of the file completely unchanged.

Write the result directly to AGENTS.md.
```
