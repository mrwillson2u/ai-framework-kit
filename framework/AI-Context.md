# AI-Context.md

> **Purpose:** This is the entry point for any AI tool working on this project.
> Read this file first to understand the project structure and how to navigate it.

---

## Project Info

| Attribute | Value |
|-----------|-------|
| **Project Name** | `[TODO]` |
| **Project Type** | `[TODO: web app, mobile app, API service, CLI tool, etc.]` |
| **Current Phase** | `[TODO: see 09-Process-Guide.md]` |

---

## File Map

All framework documents are in the `framework/` directory.

| File | What It Contains | Read Order |
|------|------------------|------------|
| `01-Concept.md` | Vision, problem, goals, users | 1st |
| `02-PRD.md` | Features, MVP scope, acceptance criteria | 2nd |
| `03-UX-Framework.md` | User research, personas, platform choice | 3rd |
| `04-Visual-Style-Guide.md` | Design tokens, colors, typography, components | 4th |
| `05-System-Architecture.md` | Tech stack, services, infra, data flow | 5th |
| `06-Data-Model.md` | Entities, relationships, schemas | 6th |
| `07-API-Contract.md` | Endpoints, protocols, interface definitions | 7th |
| `08-Decision-Log.md` | Why we chose what we chose | Reference |
| `09-Process-Guide.md` | Phase tracker and discovery overview | Meta |
| `ProcessGuide/starter_questions.md` | Full question set for discovery | Meta |

---

## Cross-References

- Architecture decisions reference entries in `08-Decision-Log.md` by ID (e.g., DEC-001)
- PRD features map to API endpoints in `07-API-Contract.md`
- Data Model entities are referenced in both Architecture and API docs
- Visual Style Guide tokens are used in UX Framework component specs
- Phase progress is tracked in `09-Process-Guide.md`

---

## AI Instructions

### During Discovery (docs empty)

1. Read `AGENTS.md` for facilitation instructions
2. Check `09-Process-Guide.md` for current phase status
3. Walk through `ProcessGuide/starter_questions.md` phase by phase
4. Update docs as answers are provided
5. Update phase tracker in `09-Process-Guide.md` as you go

### During Implementation (docs filled)

- Follow the tech stack defined in `05-System-Architecture.md`
- Follow tokens and patterns in `04-Visual-Style-Guide.md` for UI
- Check `02-PRD.md` for scope and acceptance criteria before adding features
- Reference `06-Data-Model.md` and `07-API-Contract.md` for data/API work
- Log all significant decisions in `08-Decision-Log.md`

### Formatting Standards

- Use consistent markdown: H1 for doc title, H2 for sections, H3 for subsections
- Keep tables aligned and readable
- Use `[TODO]` markers for unfilled sections
- Date format: YYYY-MM-DD
