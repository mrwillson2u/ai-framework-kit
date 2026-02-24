# Project Kickoff Framework

A reusable, AI-optimized project scaffolding kit. Each document is structured for efficient LLM ingestion and iterative AI-assisted development.

## Quick Start

### 1. Copy the framework to your new project

```bash
cp -r /path/to/framework-kit ~/projects/my-new-app
cd ~/projects/my-new-app
git init  # optional: start fresh git history
```

### 2. Tell the AI what you're building (optional but recommended)

Before starting, you can tell the AI your project type to skip irrelevant phases:

```
This is a backend service with no UI.
```

Or for existing codebases:

```
I'm adding features to an existing codebase. The code is in /src.
```

The AI will adjust the discovery flow accordingly. See [Project Types](#project-types) and [Existing Codebases](#existing-codebases) below.

### 3. Open in your AI coding tool

| Tool | Command |
|------|---------|
| **Claude Code (CLI)** | `cd ~/projects/my-new-app && claude` |
| **Claude Code (VS Code)** | Open folder in VS Code, then open Claude panel |
| **Cursor** | Open folder in Cursor |
| **Windsurf** | Open folder in Windsurf |
| **GitHub Copilot** | Open folder in VS Code with Copilot enabled |

### 3. The AI should automatically start the discovery process

The AI reads its config file (`CLAUDE.md`, `.cursorrules`, etc.), which redirects to `AGENTS.md`. This instructs it to:

1. Detect that the framework docs are empty
2. Begin the discovery questionnaire (Phase 1: Concept)
3. Ask questions one at a time
4. Populate the documents as you answer

---

## If the AI Doesn't Start Automatically

Some tools need a nudge. Paste this prompt:

```
Read AGENTS.md and follow its instructions.
```

Or be more explicit:

```
Read AGENTS.md, then framework/ProcessGuide/starter_questions.md. 
Start the discovery process — ask me the Phase 1 questions.
```

---

## Tool-Specific Tips

### Claude Code
Works best. Reads `CLAUDE.md` automatically on startup. Just open the project and it should begin.

### Cursor
Reads `.cursorrules` on startup. If it doesn't auto-start, use the prompt above. Cursor sometimes needs you to @ mention a file: `@AGENTS.md follow these instructions`.

### Windsurf
Reads `.windsurfrules` on startup. Similar to Cursor — if it doesn't auto-start, prompt it to read `AGENTS.md`.

### GitHub Copilot
Reads `.github/copilot-instructions.md`. Copilot is more passive than other tools — you'll likely need to explicitly ask it to start the discovery process.

### Other Tools / Generic LLMs
Point them at `AGENTS.md` directly:
```
Read AGENTS.md and follow its instructions for this project.
```

---

## Project Structure

```
framework-kit/
├── AGENTS.md                        # AI instructions (canonical)
├── CLAUDE.md                        # Redirect → AGENTS.md
├── .cursorrules                     # Redirect → AGENTS.md
├── .windsurfrules                   # Redirect → AGENTS.md
├── .github/
│   └── copilot-instructions.md      # Redirect → AGENTS.md
├── README.md                        # This file
└── framework/                       # All framework documents
    ├── AI-Context.md                # Project context for AI tools
    ├── 01-Concept.md                # Vision, problem, goals, users
    ├── 02-PRD.md                    # Product requirements, MVP scope
    ├── 03-UX-Framework.md           # User research, personas, platform
    ├── 04-Visual-Style-Guide.md     # Colors, typography, components
    ├── 05-System-Architecture.md    # Tech stack, services, infra
    ├── 06-Data-Model.md             # Entities, relationships, schemas
    ├── 07-API-Contract.md           # Endpoints, protocols, interfaces
    ├── 08-Decision-Log.md           # Why we chose what we chose
    ├── 09-Process-Guide.md          # Overview of discovery process
    ├── 10-UI-Generation-Prompt.md   # Generated prompt for UI tools
    └── ProcessGuide/
        └── starter_questions.md     # Full question set for discovery
```

---

## How It Works

```
┌─────────────────────────────────────────────────────────────────┐
│  You open project in AI tool                                    │
│         ↓                                                       │
│  AI reads CLAUDE.md / .cursorrules / etc.                       │
│         ↓                                                       │
│  Redirected to AGENTS.md                                        │
│         ↓                                                       │
│  AI detects empty docs → starts discovery flow                  │
│         ↓                                                       │
│  Asks questions from framework/ProcessGuide/starter_questions.md│
│         ↓                                                       │
│  Populates framework/ docs as you answer                        │
│         ↓                                                       │
│  Docs filled → AI shifts to implementation mode                 │
└─────────────────────────────────────────────────────────────────┘
```

---

## Discovery Phases

| Phase | Questions Feed Into |
|-------|---------------------|
| 1 - Concept | `framework/01-Concept.md` |
| 2 - UX & Discovery | `framework/03-UX-Framework.md` |
| 3 - Product Requirements | `framework/02-PRD.md` |
| 4 - Architecture | `framework/05-System-Architecture.md`, `06-Data-Model.md`, `07-API-Contract.md` |
| 5 - Visual Design | `framework/04-Visual-Style-Guide.md` |
| 6 - MVP & Roadmap | `framework/02-PRD.md` (MVP section), `08-Decision-Log.md` |

---

## Project Types

Not every project needs every phase. At the start of discovery, the AI will ask about your project type and automatically skip irrelevant phases.

### Common Profiles

| Project Type | Phases Used | Phases Skipped |
|--------------|-------------|----------------|
| **Full-stack web app** | All | — |
| **Backend service / API** | Concept, Requirements, Architecture, Data Model, API | UX, Visual Design |
| **CLI tool** | Concept, Requirements, Architecture | UX (mostly), Visual Design, Data Model (maybe) |
| **Library / SDK** | Concept, Requirements, Architecture, API | UX, Visual Design |
| **Mobile app** | All | — |
| **Data pipeline** | Concept, Requirements, Architecture, Data Model | UX, Visual Design, API (maybe) |

### Telling the AI Your Project Type

At the start, say something like:

- "This is a backend service with no UI"
- "I'm building a CLI tool"
- "This is an internal API — no end users"

The AI will confirm which phases to skip and proceed with the relevant ones.

---

## Existing Codebases

This framework isn't just for greenfield projects. You can use it when:

- **Adding a major feature** to an existing app
- **Refactoring or redesigning** a system
- **Documenting** an undocumented codebase
- **Planning v2** of an existing product

### How to Use with Existing Code

1. **Tell the AI about your codebase:**
   ```
   I'm adding a new feature to an existing codebase. 
   The code is in /src. Read it first to understand the current architecture.
   ```

2. **The AI will:**
   - Analyze your existing code structure
   - Pre-fill relevant sections (tech stack, data model, etc.) based on what exists
   - Focus discovery on the *new* work, not redocumenting everything

3. **Selective documentation:**
   - You can fill only the docs relevant to your change
   - e.g., for a new feature: just update PRD + relevant Architecture sections
   - e.g., for a refactor: focus on Architecture + Decision Log

### Example Prompts for Existing Codebases

```
I'm adding user authentication to this existing Express app. 
Let's document the feature using this framework.
```

```
I want to document the architecture of this codebase. 
Read the code and help me fill out the Architecture and Data Model docs.
```

```
We're planning a major refactor. Use this framework to document 
the current state and the proposed changes.
```

---

## Skipping, Resuming & Revising

### Skipping Questions

Not every question applies to every project. You can:

- Say **"skip"** or **"skip this for now"** — the AI will move on and mark it as skipped
- Say **"defer"** or **"I'll decide later"** — the AI will mark it `[TBD]` and continue

Skipped/deferred items are tracked in `framework/09-Process-Guide.md` so you can return to them.

### Resuming After a Break

If you close your session and return later:

1. Open the project in your AI tool
2. Say: **"Let's continue where we left off"** or **"Resume discovery"**
3. The AI will check `framework/09-Process-Guide.md` for phase status and pick up from there

### Revising Previous Answers

Changed your mind? Need to update something? Just tell the AI:

- **"Go back to Phase 2"** — revisit a specific phase
- **"I want to change my answer about [topic]"** — AI will find and update the relevant section
- **"Update the tech stack in the Architecture doc"** — direct edit request
- **"Let's revisit the user personas"** — reopen a specific area

The AI will update the relevant document(s) and note the change. For significant reversals, it will add an entry to `framework/08-Decision-Log.md` explaining the change.

### Checking Progress

To see what's complete and what's pending:

- Say: **"Show me the current progress"** or **"What's left to do?"**
- The AI will read `framework/09-Process-Guide.md` and summarize the status

---

## UI Generation Prompts

After completing the UX Framework and Visual Style Guide, you can generate a prompt optimized for UI design tools:

```
Generate a UI prompt for this project.
```

The AI will create a self-contained prompt in `framework/10-UI-Generation-Prompt.md` that you can paste into:

- **Google Stitch** — Full app generation
- **Vercel v0** — React/Next.js components
- **Galileo AI** — Multi-screen flows
- **Figma AI** — Design system generation

The generated prompt includes everything the UI tool needs: user context, screens, visual style, colors, typography, and features.

See `examples/task-app/framework/10-UI-Generation-Prompt.md` for a complete example.

---

## Customization

- **Edit `framework/ProcessGuide/starter_questions.md`** to add/remove/reorder discovery questions
- **Edit `AGENTS.md`** to change AI behavior or add project-specific instructions
- **Add new documents** to `framework/` as needed — update `framework/AI-Context.md` with the file map

---

## Example: TaskFlow

See `examples/task-app/` for a **fully completed example** of the framework in action. It demonstrates:

- A task management app for freelancers with time tracking
- All documents filled out with real content
- Architectural decisions documented with rationale
- Modern tech stack (Next.js, Supabase, Vercel)

Browse the example to understand what "done" looks like before starting your own project.

---

## License

MIT — use freely, modify as needed.
