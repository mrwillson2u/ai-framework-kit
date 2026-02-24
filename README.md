# Project Kickoff Framework

A reusable, AI-optimized project scaffolding kit. Each document is structured for efficient LLM ingestion and iterative AI-assisted development.

## Quick Start

### 1. Copy the framework to your new project

```bash
cp -r /path/to/framework-kit ~/projects/my-new-app
cd ~/projects/my-new-app
git init  # optional: start fresh git history
```

### 2. Open in your AI coding tool

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
Read AGENTS.md, then ProcessGuide/starter_questions.md. 
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

## Documents

| Document | Purpose |
|----------|---------|
| `AGENTS.md` | AI instructions — how to facilitate the discovery process |
| `AI-Context.md` | Project context for AI tools (file map, cross-references) |
| `ProcessGuide/starter_questions.md` | Full question set for LLM-led discovery |
| `01-Concept.md` | Vision, problem statement, goals, target users |
| `02-PRD.md` | Product requirements, features, MVP scope, acceptance criteria |
| `03-UX-Framework.md` | User research, needs discovery, personas, platform choice |
| `04-Visual-Style-Guide.md` | Colors, typography, spacing, components, tokens |
| `05-System-Architecture.md` | Tech stack, services, infra, data flow |
| `06-Data-Model.md` | Entities, relationships, schemas |
| `07-API-Contract.md` | Endpoints, protocols, interface definitions |
| `08-Decision-Log.md` | Why we chose what we chose |
| `09-Process-Guide.md` | Overview of the LLM-led discovery process |

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
│  Asks questions from ProcessGuide/starter_questions.md          │
│         ↓                                                       │
│  Populates framework docs as you answer                         │
│         ↓                                                       │
│  Docs filled → AI shifts to implementation mode                 │
└─────────────────────────────────────────────────────────────────┘
```

---

## Discovery Phases

| Phase | Questions Feed Into |
|-------|---------------------|
| 1 - Concept | `01-Concept.md` |
| 2 - UX & Discovery | `03-UX-Framework.md` |
| 3 - Product Requirements | `02-PRD.md` |
| 4 - Architecture | `05-System-Architecture.md`, `06-Data-Model.md`, `07-API-Contract.md` |
| 5 - Visual Design | `04-Visual-Style-Guide.md` |
| 6 - MVP & Roadmap | `02-PRD.md` (MVP section), `08-Decision-Log.md` |

---

## Customization

- **Edit `ProcessGuide/starter_questions.md`** to add/remove/reorder discovery questions
- **Edit `AGENTS.md`** to change AI behavior or add project-specific instructions
- **Add new documents** as needed — just update `AI-Context.md` with the file map

---

## License

MIT — use freely, modify as needed.
