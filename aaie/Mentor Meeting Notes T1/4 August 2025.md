# Weekly Mentor Meeting Summary Notes

**Date:** August 4, 2025  

---

## Project Updates and Scrum Progress

- **Scrum Process:** All teams reported positive momentum. Sprint 2 is on track.

- **Data Team:**
  - GitHub workflow implemented.
  - Receiving updated requirements from LLM team; new data structuring in progress.
  - Pivot involves light restructuring, reusing existing formats.

- **Short-Term Dataset:**
  - Data team to deliver a new set of 30 annotated submissions (5 subjects × 2 assignments × 3 types: AI, Human, Hybrid).
  - Each submission includes matching feedback based on 10 rubrics.
  - Delivery target: **Wednesday August 6, 2025**.

---

## LLM Team Progress

- No PO/stakeholder meeting held this week.

- **Product feedback from prior meeting:**
  - Document all research and maintain a central documentation repo (including notes, prompt experiments, etc.).

- **LLM Work Focus:**
  - Exploring prompt engineering and model evaluation for:
    - AI detection (3-class: Human / AI / Hybrid only — no percentage)
    - Feedback generation
  - Revision chains currently out of scope.

- **Constraints:**
  - Percent score for AI detection infeasible without fine-tuning; shifted to label-only output.
  - Product team has shared an API proposal; yet to be validated against LLM integration needs.

---

## Product & API Discussion

- **SRS and API Proposal:**
  - Created initial Software Requirement Specification (SRS) and draft API list.
  - Collaboration started with backend team; discussed integration needs with LLM team.
  - Shared a benchmarking dataset from the mentor with the data team.
  - **Action Item:** Share all relevant information openly on team channels, not just DMs.

- **API Review Feedback:**
  - Kasfi’s proposal included endpoints for:
    - Uploads (prompts, student responses, chatlogs)
    - Rubric management
    - Submission review + reports
    - Revision history
  - **Issues raised:**
    - Several endpoints not aligned with current MVP scope (e.g., predefined prompts).
    - Mentor advised clearly labelling MVP vs future endpoints in documentation.
    - Use use-case diagrams to connect endpoints to functional roles.

- **Design/System Planning:**
  - Created internal diagrams showing system actors, functional modules, and workflows.
  - Endpoints grouped by phase:
    - **Phase 1 (MVP):** Educator-only use cases
    - **Phase 2:** Student-facing features and advanced analytics
  - Mentor emphasized splitting API ownership:
    - APIs from LLM team (AI scoring, feedback generation)
    - Frontend/backend APIs consumed by platform users

- **Key Alignment Gaps Identified:**
  - Teams using 2–3 different API documents.
  - Proposal for creating separate documents for MVP vs Future APIs.
  - Mentor agreed: Maintain one clean version with a column indicating “Now / Future”.

---

## Collaboration and Communication Practices

- All documentation (SRS, use cases, API specs) must be shared in team channels by default.
- Communication leads should monitor information clarity and flow on Slack/Discord.
- Design feedback should be surfaced in mentor meetings for cross-pillar discussion.

---

## Next Steps & Decisions

| Action Item | Owner(s) | Due Date |
|-------------|----------|----------|
| Finalize MVP-labelled API table | Product Team | Before next mentor meeting |
| Refactor documentation into one shared SRS repo | Arnav, Monique, Kasfi | Ongoing |
| Share benchmark dataset format and link in public channel | Kasfi | Immediate |
| Sync between LLM & Product/API teams to confirm which endpoints will be available | Arnav, Kasfi | This week |
| Begin implementation within Phase 1 (Educator-only) scope | Product Team | Current Sprint |
| Prepare use-case–linked API flow diagrams | Negin, Yugam | ASAP |

---

## Clarifications

- MVP focuses only on educator-facing features.
- Students will not have access to the platform this trimester.
- LLM-generated outputs will use label classification (AI/Human/Hybrid), not percentages.
- RBAC (Role-Based Access Control) is moved to future scope for now.
- Future features like AI score highlighting or edit trace detection are deferred to Trimester 3.
