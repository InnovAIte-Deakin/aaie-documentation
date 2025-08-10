# First Product Owner Meeting Notes

**Date:** 25 July 2025  

---

## MEETING CONTEXT
- **Purpose:** Initial consultation with the PO to align project understanding, data ethics, deliverables, technical feasibility, and future vision.

---

## 1. Project Clarifications & Ethical Guidance

### Project Ownership and Confidentiality
- The project is owned by Deakin and students should refrain from sharing internal details with external parties.
- The project is still in development and Dr. Ofoghi is actively shaping its direction.

### External Dataset Usage – Critical Advisory
- Lucy discussed using a public dataset from a Korean research group, with Creative Commons licensing and restricted redistribution.
- **Dr. Ofoghi’s instructions:**
  - Do not sign or submit any external consent forms individually.
  - Do not communicate directly with data owners for approval — always route through PO or mentor.
  - Any dataset or communication involving IP or usage rights must be reviewed and approved to avoid potential IP conflicts or shared ownership concerns.

---

## 2. Synthetic Data Strategy

**Why Synthetic Data?**
- If suitable public datasets are unavailable, teams are encouraged to generate synthetic data using GenAI.
- This can include:
  - Synthetic rubrics
  - Synthetic essay responses
  - Synthetic feedback

---

## 3. Fine-Tuning vs. Few-Shot Learning

### Why Fine-Tuning Was Discouraged
- Initially, the LLM team planned to fine-tune mini LLMs.
- PO advised against it due to:
  - High resource demands (took him over a month to set up LLaMA 2 7B)
  - Need for exact environment versions
  - Risk of bad outputs if data quality is low
  - Storage complexity and GPU access limitations

### Alternatives Proposed
- **Few-Shot Learning:** Provide several input-output examples to guide LLM behavior.
- **Zero-Shot Learning:** No examples needed; rely purely on prompt design.

> **NOTE:** At this stage, we need functionality and a working framework — not heavy retraining. The model will eventually be replaced with a custom-built LLM anyway.

**Action**
- LLM team to pause fine-tuning efforts, re-evaluate tasks, and possibly pivot to few-shot/zero-shot learning for now.

---

## 4. Final Product Vision & Capabilities

### Phase 1 Capabilities (Immediate Scope)
- Upload student submissions
- Generate AI-based feedback (clarity, structure, relevance)
- Detect AI-generated content in writing
- Provide plagiarism score
- Results available only to educators

### Phase 2+ Vision (1–2 Years)
- Students will be allowed to use GenAI tools but must:
  - Submit prompts used
  - Submit intermediate outputs
  - Submit a final human-written synthesis
- System should:
  - Analyze prompt-to-output alignment
  - Evaluate authenticity of final work
  - Ensure student contribution and prevent overuse of GenAI

### Constraints
- Full essays generated solely by LLMs are not acceptable.
- Final outputs must demonstrate human critical thinking, rewriting, and interpretation.

---

## 5. System Design Discussions
- Students should not receive direct feedback or flag scores.
- All interaction with flagged results is limited to educators.
- Access levels must be differentiated by user role (student vs. educator).

---

## 6. Data Schema & Traceability
PO wants final submission to be:
- Student-written, not copied from LLM
- Show clear distinction and traceability from LLM outputs

**Goal:** The system should be able to assess:
- Prompt validity
- Whether intermediate outputs match the prompts
- Whether final work is coherently built by the student

---

## Action Items Summary

| Who         | Action |
|-------------|--------|
| All teams   | Avoid external dataset agreements without PO review |
| Data Team   | Proceed with hybrid/synthetic dataset generation |
| LLM Team    | Pause fine-tuning; shift to few-/zero-shot learning |
| Design Team | Update system design & access levels based on feedback |
| Entire Team | Align future development with evolving scope and vision |
