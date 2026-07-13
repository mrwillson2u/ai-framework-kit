# Process Guide

> **Purpose:** Ship target, phase tracker, and current project state.

---

## Ship Target

*(Set during Phase 6. This is the project's definition of done — see Ship Discipline in `AGENTS.md`.)*

| Attribute | Value |
|-----------|-------|
| **Smallest Publishable Version (SPV)** | `[TODO: concrete, checkable definition — e.g., "auth + task CRUD + Today View, live at the domain"]` |
| **Ship Date** | `[TODO: YYYY-MM-DD — a hard date]` |
| **Deploy Target / Domain** | `[TODO: where it goes live and how users reach it]` |
| **Status** | `[TODO: Not set / On track / Overdue / Shipped YYYY-MM-DD]` |

After the SPV is defined: scope additions go to the Post-Ship Backlog in `02-PRD.md` unless they block the SPV (DEC-XXX entry required). If the date passes, cut scope rather than extend — date extensions also require a DEC-XXX entry.

---

## Project Context

| Attribute | Value |
|-----------|-------|
| **Project Type** | `[TODO: web app, backend service, CLI, library, etc.]` |
| **Scope** | `[TODO: new project / adding features / refactor / documentation]` |
| **Existing Codebase** | `[TODO: Yes (path) / No]` |

---

## Current Phase

**Status:** `[TODO: Not Started / In Progress / Complete]`

| Phase | Status | Last Updated | Notes |
|-------|--------|--------------|-------|
| 0 - Scoping | ⬜ Not Started | | Complete only when AI-Context Project Summary is populated |
| 1 - Concept | ⬜ Not Started | | |
| 2 - UX & Discovery | ⬜ Not Started | | |
| 3 - Product Requirements | ⬜ Not Started | | |
| 4 - Architecture | ⬜ Not Started | | |
| 5 - Visual Design | ⬜ Not Started | | |
| 6 - MVP & Roadmap | ⬜ Not Started | | Sets the Ship Target above |
| 7 - Ship | ⬜ Not Started | | Done = SPV live |

**Legend:** ⬜ Not Started | 🟡 In Progress | ✅ Complete | ⏭️ Skipped (N/A for this project)

---

## How Discovery Works

The AI facilitator follows `AGENTS.md` (the canonical instruction file) and asks the questions in `ProcessGuide/starter_questions.md`, phase by phase, populating the framework docs as you answer. For small/solo projects, aim to finish Phases 0–6 in one sitting.

To resume after a break, tell the AI: *"Let's continue where we left off"* — it checks the tracker above and picks up from the first incomplete phase.

---

## Phase Details

### Phase 0: Scoping
**Output:** Project Context (above), Project Summary in `AI-Context.md`
**Focus:** What's being built, new vs. existing code, which phases apply

### Phase 1: Concept
**Output:** `01-Concept.md`
**Focus:** Problem, vision, users, goals, constraints, risks

### Phase 2: UX & Discovery
**Output:** `03-UX-Framework.md`
**Focus:** User journeys, personas, platform selection, accessibility

### Phase 3: Product Requirements
**Output:** `02-PRD.md`
**Focus:** Features, MVP scope, acceptance criteria, priorities

### Phase 4: Architecture
**Output:** `05-System-Architecture.md`, `06-Data-Model.md`, `07-API-Contract.md`
**Focus:** Tech stack, services, data flow, NFRs, API design, test/deploy pipeline

### Phase 5: Visual Design
**Output:** `04-Visual-Style-Guide.md`
**Focus:** Colors, typography, components, design tokens

### Phase 6: MVP & Roadmap
**Output:** `02-PRD.md` (MVP section), `08-Decision-Log.md`, Ship Target (above)
**Focus:** MVP definition, SPV, ship date, milestones, first build steps

### Phase 7: Ship
**Output:** The SPV, live
**Focus:** Unblocking, cutting scope, deploying — see the Phase 7 checklist in `starter_questions.md`

---

## Skipped / Deferred Items

Not every question applies — "skip" and "defer" are valid answers (mechanics in `AGENTS.md`). The AI tracks them here:

| Item | Phase | Status | Reason | Resolved |
|------|-------|--------|--------|----------|
| *Example: Accessibility requirements* | *2* | *Deferred* | *Need to research WCAG standards* | *⬜* |

**Status:** Skipped (N/A for this project) | Deferred (TBD, will revisit)
**Resolved:** ⬜ Pending | ✅ Done

---

## Revisions

*(AI logs significant changes to previous answers here; major reversals also get a DEC-XXX entry)*

| Date | What Changed | Document | Reason |
|------|--------------|----------|--------|
| | | | |

---

## After the SPV Ships

1. Mark the Ship Target status **Shipped** with the actual date, and log it as a DEC-XXX entry
2. The numbered docs (01–07, 10) become advisory/historical — only the Project Summary in `AI-Context.md` and the Decision Log stay current
3. Pull the next work from the Post-Ship Backlog in `02-PRD.md`

---

## Session Notes

*(AI or user can log notes about each session here. Longer transcripts can go in `session-logs/`, which is git-ignored.)*

| Date | Note |
|------|------|
| | |
