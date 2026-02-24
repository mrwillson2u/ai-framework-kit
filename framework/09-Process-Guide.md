# Process Guide

> **Purpose:** Overview of the LLM-led discovery process and current project state.

---

## Current Phase

**Status:** `[TODO: Not Started / In Progress / Complete]`

| Phase | Status | Last Updated |
|-------|--------|--------------|
| 1 - Concept | ⬜ Not Started | |
| 2 - UX & Discovery | ⬜ Not Started | |
| 3 - Product Requirements | ⬜ Not Started | |
| 4 - Architecture | ⬜ Not Started | |
| 5 - Visual Design | ⬜ Not Started | |
| 6 - MVP & Roadmap | ⬜ Not Started | |

**Legend:** ⬜ Not Started | 🟡 In Progress | ✅ Complete | ⏭️ Skipped

---

## Discovery Process

### How It Works

1. **AI facilitator** reads `AGENTS.md` and `ProcessGuide/starter_questions.md`
2. Walks through each phase, asking questions conversationally
3. Populates framework docs based on your answers
4. Summarizes each phase before moving on
5. Once complete, shifts to implementation mode

### Resuming a Session

If you return after interruption:
- Check the phase tracker above to see where you left off
- Tell the AI: "Resume from Phase X"
- Or: "Let's continue where we left off"

---

## Phase Details

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
**Focus:** Tech stack, services, data flow, NFRs, API design

### Phase 5: Visual Design
**Output:** `04-Visual-Style-Guide.md`
**Focus:** Colors, typography, components, design tokens

### Phase 6: MVP & Roadmap
**Output:** `02-PRD.md` (MVP section), `08-Decision-Log.md`
**Focus:** MVP definition, milestones, first steps, logging decisions

---

## Skipping & Deferring

Not every question applies to every project. It's okay to:

- **Skip** questions that don't apply (e.g., no compliance requirements)
- **Defer** decisions for later (note as "TBD" with reasoning)
- **Come back** to any phase to add detail

Tell the AI: "Skip this for now" or "Defer — we'll decide later"

### Skipped / Deferred Items

*(AI updates this list when items are skipped or deferred)*

| Item | Phase | Status | Reason | Resolved |
|------|-------|--------|--------|----------|
| *Example: Accessibility requirements* | *2* | *Deferred* | *Need to research WCAG standards* | *⬜* |

**Status:** Skipped (N/A for this project) | Deferred (TBD, will revisit)
**Resolved:** ⬜ Pending | ✅ Done

---

## Revisions

*(AI logs significant changes to previous answers here)*

| Date | What Changed | Document | Reason |
|------|--------------|----------|--------|
| | | | |

---

## Post-Discovery

Once all phases are complete:

1. **Review** all generated docs for accuracy
2. **Refine** any sections that need more detail
3. **Begin implementation** — AI should reference Architecture and PRD
4. **Update docs** as the project evolves

---

## Session Notes

*(AI or user can log notes about the discovery session here)*

| Date | Note |
|------|------|
| | |
