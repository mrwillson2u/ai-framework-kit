# AI-Context.md

> **Purpose:** This is the entry point for any AI tool working on this project.
> Read this file first to understand the project structure and how to navigate it.

---

## Project Type

`[TODO: e.g. web app, mobile app, API service, CLI tool, etc.]`

## File Map

All framework documents are in the `framework/` directory.

| File | What It Contains | Read Order |
|---|---|---|
| `01-Concept.md` | Vision, problem, goals, users | 1st |
| `02-PRD.md` | Features, MVP scope, acceptance criteria | 2nd |
| `03-UX-Framework.md` | User research, personas, platform choice | 3rd |
| `04-Visual-Style-Guide.md` | Design tokens, colors, typography, components | 4th |
| `05-System-Architecture.md` | Tech stack, services, infra, data flow | 5th |
| `06-Data-Model.md` | Entities, relationships, schemas | 6th |
| `07-API-Contract.md` | Endpoints, protocols, interface definitions | 7th |
| `08-Decision-Log.md` | Why we chose what we chose | Reference |
| `09-Process-Guide.md` | LLM-led discovery questionnaire | Meta |
| `ProcessGuide/starter_questions.md` | Full question set for discovery | Meta |

## Cross-References

- Architecture decisions reference entries in `08-Decision-Log.md` by ID
- PRD features map to API endpoints in `07-API-Contract.md`
- Data Model entities are referenced in both Architecture and API docs
- Visual Style Guide tokens are used in UX Framework component specs

## AI Instructions

- When generating code, follow the tech stack defined in `05-System-Architecture.md`
- When creating UI, follow tokens and patterns in `04-Visual-Style-Guide.md`
- When adding features, check `02-PRD.md` for scope and acceptance criteria
- Log all significant decisions in `08-Decision-Log.md`
- Use consistent markdown formatting: H1 for doc title, H2 for sections, H3 for subsections
