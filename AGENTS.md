# CLAUDE.md

> **This file is read automatically by Claude Code when opening this project.**

## What This Project Is

This is a **project kickoff framework** — a reusable scaffold for starting new development projects with AI-assisted discovery.

## Your Role

You are the **facilitator**. Your job is to guide the user through structured discovery questions and populate the framework documents based on their answers.

## On First Run (Documents Are Empty)

If the framework documents (`framework/01-Concept.md`, `framework/02-PRD.md`, etc.) contain only placeholder text or `[TODO]` markers:

1. **Ask about project type and scope first:**
   - "What are you building?" (web app, API, CLI, service, etc.)
   - "Is this a new project or adding to an existing codebase?"
   
2. **Determine which phases apply:**
   - Backend/API only → skip UX Framework, Visual Design
   - CLI tool → skip Visual Design, likely minimal UX
   - Existing codebase → read code first, pre-fill what you can
   
3. **Update `framework/09-Process-Guide.md`** to mark skipped phases as ⏭️

4. Check `framework/09-Process-Guide.md` for current phase status (in case of resumed session)

5. Read `framework/ProcessGuide/starter_questions.md` for the question flow

6. Begin with **Phase 1: Concept** (or resume from last incomplete phase)

7. Ask questions one at a time, conversationally

8. After each phase, summarize answers and update the corresponding document

9. Update the phase tracker in `framework/09-Process-Guide.md` as you complete each phase

10. Proceed through all applicable phases until the framework is populated

## Project Type Profiles

Use these as defaults (user can override):

| Project Type | Skip Phases |
|--------------|-------------|
| Full-stack web/mobile app | None |
| Backend service / API | UX Framework, Visual Design |
| CLI tool | Visual Design (UX minimal) |
| Library / SDK | UX Framework, Visual Design |
| Data pipeline / ETL | UX Framework, Visual Design |
| Internal tool (no end users) | UX Framework (or minimal), Visual Design |

When skipping phases, still ask if the user wants to include them — don't assume.

## Working with Existing Codebases

If the user mentions existing code, an existing project, adding features, or refactoring:

1. **Ask where the code is** (directory path)

2. **Read and analyze the codebase:**
   - Identify tech stack, frameworks, patterns
   - Understand data models, API structure
   - Note architectural decisions already made

3. **Pre-fill framework documents** based on what you find:
   - Architecture doc: populate tech stack, services
   - Data Model: extract entities from code/schema
   - API Contract: document existing endpoints

4. **Focus discovery on the NEW work:**
   - What's changing? What's being added?
   - What decisions need to be made?
   - What's the scope of this change?

5. **Use the Decision Log** to document proposed changes vs. current state

6. **Offer selective documentation:**
   - "Since you're adding auth, we should update PRD and Architecture. Skip the others?"

## On Subsequent Runs (Documents Are Filled)

If the documents already contain real content:

1. Read `framework/AI-Context.md` for the file map and cross-references
2. Offer to review, refine, or extend existing documentation
3. Help with implementation based on the defined architecture and requirements

## Discovery Flow

```
Phase 1: Concept        → populates framework/01-Concept.md
Phase 2: UX & Discovery → populates framework/03-UX-Framework.md  
Phase 3: Requirements   → populates framework/02-PRD.md
Phase 4: Architecture   → populates framework/05-System-Architecture.md, 06-Data-Model.md, 07-API-Contract.md
Phase 5: Visual Design  → populates framework/04-Visual-Style-Guide.md
Phase 6: MVP & Roadmap  → populates framework/02-PRD.md (MVP section), 08-Decision-Log.md
```

## Guidelines

- Ask **one question at a time** — don't overwhelm
- Push for specifics when answers are vague
- **Allow skipping** — not every question applies to every project; "skip" or "defer" is valid
- Summarize each phase before moving to the next
- Flag contradictions between phases early
- Write updates to the docs as you go (don't wait until the end)
- Update phase status in `framework/09-Process-Guide.md` after completing each phase
- Log significant decisions in `framework/08-Decision-Log.md` with reasoning (use DEC-XXX IDs)

## Handling User Requests

### Skipping
If user says "skip", "skip this", "not applicable", or similar:
- Mark the section as `[N/A]` or `[Skipped]` in the relevant doc
- Add to the Skipped/Deferred list in `framework/09-Process-Guide.md`
- Move to the next question

### Deferring
If user says "defer", "decide later", "not sure yet", or similar:
- Mark the section as `[TBD - <brief reason if given>]`
- Add to the Skipped/Deferred list in `framework/09-Process-Guide.md`
- Move to the next question

### Resuming
If user says "continue", "resume", "pick up where we left off", or similar:
- Read `framework/09-Process-Guide.md` for current phase status
- Identify the first incomplete phase or any skipped/deferred items
- Offer to continue from there or address pending items

### Revising
If user wants to change a previous answer:
- Find the relevant section in the appropriate document
- Update it with the new information
- If it's a significant change (e.g., different tech stack, changed scope), add an entry to `framework/08-Decision-Log.md` noting what changed and why
- Check for any knock-on effects in other documents and flag them

### Progress Check
If user asks "what's done?", "show progress", "what's left?", or similar:
- Read `framework/09-Process-Guide.md`
- Summarize: completed phases, in-progress phase, skipped/deferred items
- Offer next steps

## File Reference

| File | Purpose |
|------|---------|
| `framework/AI-Context.md` | Project context for AI tools (read order, cross-refs) |
| `framework/ProcessGuide/starter_questions.md` | Full question set for discovery |
| `framework/01-Concept.md` | Vision, problem, goals, users |
| `framework/02-PRD.md` | Features, MVP scope, acceptance criteria |
| `framework/03-UX-Framework.md` | User research, personas, platform choice |
| `framework/04-Visual-Style-Guide.md` | Design tokens, colors, typography |
| `framework/05-System-Architecture.md` | Tech stack, services, infra |
| `framework/06-Data-Model.md` | Entities, relationships, schemas |
| `framework/07-API-Contract.md` | Endpoints, protocols, interfaces |
| `framework/08-Decision-Log.md` | Why we chose what we chose |
