# Data Curation & Generation Pillar – Current Plans (T2 2025)  

> **Status: Active**  
> This document outlines the **current plans, deliverables, and objectives** for the Data Curation & Generation Pillar of the AAIE project.  

---

## Overview, Goals, and Objectives  

The **Data Curation & Generation Pillar** is responsible for developing and maintaining the unified dataset that powers all AAIE subprojects. This dataset captures:  

- Rubric-based academic prompts and assignments  
- AI-assisted and human-style interactions  
- Multi-band student-like submissions (Excellent → Poor)  
- Feedback and revision workflows  

Our goal is to deliver a **scalable, ethics-compliant, and reproducible dataset pipeline** that supports model training, evaluation, and product integration.  

---

## Aims for Trimester (T2 2025)  

- Curate **1000+ rubrics** across at least 5 academic domains  
- Generate and validate **5000+ submissions** with quality-band coverage  
- Introduce **weighted rubrics** to reflect real-world assessment practices  
- Annotate submissions with **diverse feedback types** (excellent → poor, rubric-aligned, holistic)  
- Build initial **revision chains** to model multi-turn student–LLM workflows  
- Establish **coverage analysis tools** to track dataset balance across domains and quality levels  
- Deliver a fully **ethics-compliant and peer-reviewed dataset pipeline**  

---

## Deliverables  

### General  
- Unified **JSON schema** and documentation (`schema/schema.json`, `schema_reference.md`)  
- **Validation tools** (local `validation.py` + CI-based GitHub Actions)  
- GitHub **workflow documentation** (contributor guide, reviewer guide, setup instructions)  
- Automated **reporting scripts** for domain/quality coverage  

---

### Unified Dataset (Current Focus)  

- **100+ curated rubrics** completed (increasing weekly)  
- Each rubric includes:  
  - Prompt and full rubric with weighted criteria  
  - 5 quality-banded submissions (Excellent → Poor)  
  - LLM questions/answers and final submission text  
  - Feedback (rubric-aligned + general comments)  

- **Synthetic + human-style submissions** generated via prompt engineering  
- Validation Scripts ensures **schema compliance** before merging  

---

### Feedback & Revision Dataset (Emerging)  

- Variants of feedback:  
  - Rubric-aligned criterion comments  
  - Holistic overall comments  
  - Inline-style suggestions (planned for future)  
- Early work on **revision chains** to simulate iterative student–LLM use  

---

## Long-Term Deliverables  

- Expand dataset to **1000+ rubrics and submissions** across multiple domains  
- Extend schema to support:  
  - **Multi-turn revision chains**  
  - **Feedback variants** at criterion, holistic, and inline levels  
  - **Public dataset conversion** into AAIE schema  
- Build **reporting dashboards** for domain and quality coverage  
- Establish **dataset governance process** for future trimesters  
- Support additional assignment types (math, coding, multimodal responses)  

---

*This document represents the current active plan for the Data Curation & Generation Pillar (T2 2025). All contributors must follow the unified schema, GitHub workflows, and validation processes as documented in the [aaie-documentation repository](https://github.com/InnovAIte-Deakin/aaie-documentation).*  
