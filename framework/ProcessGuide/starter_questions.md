# Starter Questions for AI-Led Discovery

> **How to use:** An LLM walks through each phase in order, asking these questions conversationally. Answers feed into the corresponding framework docs (see Output Mapping at the end).
>
> Feel free to add, remove, or reorder questions per project.

---

## Phase 0: Project Scoping

**Output → 09-Process-Guide.md (Project Context section)**

*Ask these first to determine which phases apply:*

1. **What are you building?**
   - Web application
   - Mobile app
   - Backend service / API
   - CLI tool
   - Library / SDK
   - Data pipeline
   - Other: ___

2. **Is this a new project or existing codebase?**
   - New project (starting from scratch)
   - Adding features to existing code
   - Refactoring / redesigning existing system
   - Documenting existing system

3. **If existing codebase:** Where is the code? (path or repo URL)

4. **Does this project have end users with a UI?**
   - Yes → include UX & Visual Design phases
   - No (backend only, internal service, etc.) → skip those phases

5. **Confirm phase selection:**
   Based on your answers, here are the phases we'll cover: [list]
   Does this look right, or should we add/remove any?

*After this phase, update `09-Process-Guide.md` with project type and mark skipped phases as ⏭️*

---

## Phase 1: Concept

**Output → 01-Concept.md**

1. What is the core problem or opportunity you want to address?
2. Why does this matter now? What's the urgency or catalyst?
3. Who are the primary target users? Secondary users?
4. What does success look like? Name 2-3 measurable outcomes.
5. What are the top 3 risks or unknowns?
6. What constraints exist?
   - Timeline
   - Budget
   - Compliance / regulatory
   - Technical limitations
7. What exists today that partially solves this? How would this be different?

---

## Phase 2: User Experience & Discovery

**Output → 03-UX-Framework.md**

1. Describe the main user journey from start to finish.
2. What are the key user needs, pains, and jobs-to-be-done?
3. Are there distinct user personas? Describe each briefly.
4. Which platforms are in scope? (web, mobile, desktop, embedded, other)
5. What factors drive the platform choice? (audience behavior, offline needs, device constraints)
6. What accessibility requirements should we plan for?
7. Are there existing workflows or tools users currently rely on?
8. What would make a user choose this over the status quo?

---

## Phase 3: Product Requirements

**Output → 02-PRD.md**

1. List the core features for an MVP. What's the minimum to deliver value?
2. For each feature, what is the acceptance criteria? (How do we know it works?)
3. What features are explicitly out of scope for MVP?
4. How should features be prioritized? (Must-have / Should-have / Nice-to-have)
5. Are there any integration requirements with existing systems?
6. What does the release timeline look like? Any hard deadlines?

---

## Phase 4: System Architecture

**Output → 05-System-Architecture.md, 06-Data-Model.md, 07-API-Contract.md**

1. What are the core services or components in the system?
2. How do they interact? (sync/async, events, APIs, queues)
3. What data flows between services?
4. What are the key entities and their relationships?
5. What non-functional requirements matter most?
   - Scalability
   - Reliability / uptime
   - Security / auth
   - Observability / monitoring
6. Preferred cloud provider or hosting model? Region preferences?
7. What's the proposed tech stack? (language, framework, database, infra)
8. Why this stack over alternatives? (capture reasoning for Decision Log)
9. What are the main API endpoints or interface contracts?

---

## Phase 5: Visual Design

**Output → 04-Visual-Style-Guide.md**

1. What is the overall visual tone? (minimal, playful, corporate, bold, etc.)
2. Are there existing brand guidelines, colors, or fonts to follow?
3. What design system or component library will be used (if any)?
4. What are the target performance metrics? (LCP, CLS, FCP)
5. Are there reference apps or sites whose design you admire?
6. Dark mode, light mode, or both?

---

## Phase 6: MVP Definition & Roadmap

**Output → 02-PRD.md (MVP section), 08-Decision-Log.md**

1. Summarize the MVP feature set in one sentence.
2. What is the success metric for the MVP launch?
3. What's the rough timeline? (weeks/months)
4. What are the key milestones between now and launch?
5. What's the first thing to build? Why?
6. What decisions have been made so far that should be logged?

---

## Output Mapping

| Phase | Questions Feed Into |
|---|---|
| 0 - Project Scoping | 09-Process-Guide.md (Project Context) |
| 1 - Concept | 01-Concept.md |
| 2 - UX & Discovery | 03-UX-Framework.md |
| 3 - Product Requirements | 02-PRD.md |
| 4 - Architecture | 05-System-Architecture.md, 06-Data-Model.md, 07-API-Contract.md |
| 5 - Visual Design | 04-Visual-Style-Guide.md |
| 6 - MVP & Roadmap | 02-PRD.md (MVP section), 08-Decision-Log.md |

## Tips for AI-Led Sessions

- Ask one phase at a time; don't overwhelm
- Follow up on vague answers — push for specifics
- **Allow skipping** — "skip" or "defer" is valid if a question doesn't apply
- Summarize each phase before moving to the next
- Flag contradictions between phases early
- Update the phase tracker in `09-Process-Guide.md` as phases complete
- After all phases, generate a draft of each doc and ask for review

## Handling "Skip" and "Defer"

- **Skip:** Question doesn't apply to this project — leave section blank or note "N/A"
- **Defer:** Decision can't be made yet — mark as `[TBD]` with a note on what's blocking
- Either response is valid; don't force answers that aren't ready

## Working with Existing Codebases

When the user has existing code:

1. **Read the codebase first** before asking architecture questions
2. **Pre-fill what you can** — tech stack, patterns, data models
3. **Focus on what's new** — don't re-document everything
4. **Frame questions as "what's changing"** not "what is it"
5. **Use Decision Log** to capture before/after for significant changes

Example reframing:
- Instead of: "What's the tech stack?"
- Ask: "I see you're using Express + PostgreSQL. Are you keeping that stack or considering changes?"
