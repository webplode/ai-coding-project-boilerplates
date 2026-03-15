# Prompt: Generate AGENTS.md for a Greenfield Project

> Copy this prompt and paste it into your AI coding agent (Claude Code, Cursor, etc.) at the start of a new project. Answer the questions, then let the agent fill in your AGENTS.md boilerplate.

---

## The Prompt

```
I'm setting up a new project and need you to fill in the AGENTS.md boilerplate template.

Here are the project details:

**Project Name:** <your project name>

**What it does (1-3 sentences):**
<describe what the system will do, who will use it, and what problem it solves>

**Tech Stack:**
- Backend: <e.g., Node.js + TypeScript + NestJS, Python + FastAPI, Go, Rust + Actix, Ruby + Rails>
- Frontend: <e.g., React + TypeScript + Vite, Vue 3 + Nuxt, SvelteKit, Next.js — or "none" for backend-only>
- Database: <e.g., PostgreSQL + TypeORM, MongoDB + Mongoose, SQLite, DynamoDB>
- Queue/Workers: <e.g., BullMQ + Redis, Celery, Sidekiq — or "none">
- Auth: <e.g., Passport.js JWT, Auth0, Supabase Auth, custom — or "none yet">
- Package Manager: <e.g., npm, pnpm, cargo, poetry, go mod>

**Planned Architecture (pick or describe):**
- [ ] Monolith
- [ ] Monorepo (frontend + backend)
- [ ] Microservices
- [ ] Serverless
- [ ] Other: <describe>

**Planned Directory Structure (if you have one, otherwise say "use convention for my stack"):**
<paste your planned structure or say "use convention">

**Key Design Decisions (list any non-obvious choices you've already made):**
<e.g., "multi-tenant with row-level security", "event-sourced", "offline-first", "SSR only">

**Build & Lint Commands:**
- Backend build: <e.g., npm run build, cargo build, python -m pytest>
- Backend lint: <e.g., npm run lint, cargo clippy, ruff check .>
- Frontend build: <e.g., npm run build, N/A>
- Frontend lint: <e.g., npm run lint, N/A>

---

Now, using the AGENTS.md boilerplate template in this repo:

1. Replace ALL `<placeholder>` values and `<!-- CUSTOMIZE: -->` comments with the real values from above.
2. For the Architecture diagram, create an ASCII diagram that matches my actual stack and planned architecture.
3. For the Workspace Structure, generate the conventional directory tree for my chosen stack (or use the one I provided).
4. For Key Files, list the entry points and critical files that will exist for this stack (use the conventional names).
5. For Key Dependencies tables, list the core packages I'll need for this stack.
6. For Compiler Checks, fill in the actual commands for my stack.
7. Remove all `<!-- CUSTOMIZE: -->` HTML comments from the final output — the file should look like it was written for this project, not like a template.
8. Keep ALL sections from "MCP Agent Mail" to the end of the file completely unchanged.

Write the result directly to AGENTS.md.
```
