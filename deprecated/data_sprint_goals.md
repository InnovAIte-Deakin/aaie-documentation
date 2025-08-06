# \[DEPRECATED\]Sprint Planning Goals

This document outlines the sprint objectives for the Data Pillar of the AAIE project.

---

## Sprint 1: Week 4–6

**Focus:** Data sourcing, schema setup, pipeline foundations  
**Sprint Goal:** Establish the foundational infrastructure and pipelines for all three datasets. Source and clean ethically safe data, generate synthetic samples, and validate schemas to ensure consistency and alignment across the project.

### Goals per Dataset

#### 1. Submission Classification (AI Detection)
- Finalize and validate CSV schema  
- Source and clean ~1000 human submissions  
- Generate ~800 AI-written samples using GenAI  
- Merge and QA `submission_classification.csv`

#### 2. Feedback Annotation
- Finalize JSON schema  
- Source rubric-linked datasets (e.g., DREsS, ASAP)  
- Begin mapping rubric-annotated samples  
- QA at least 500 human samples with rubric feedback  
- Generate ~100 AI submissions with per-criterion rubric feedback

#### 3. Revision Chain
- Finalize JSON schema and validation script  
- Review IteraTe and RE3 dataset for compatibility  
- Extract and map ~600 real revision chains  
- Generate ~200 synthetic revision chains using GenAI  
- Design prompt templates (clarification, restructure, polish)  
- Write scripts to simulate AI-human revision steps

### Sprint 1 Deliverables (Data Pillar)
- Validated schemas (CSV & JSON) and documentation  
- Cleaned and partially labeled datasets  
- Working scripts for AI generation and data conversion  
- Shared repo with folder structure, README, and sample entries

---

## Sprint 2: Week 7–9

**Focus:** Dataset completion, QA, and preparation for handoff  
**Sprint Goal:** Complete and QA all datasets to prepare for downstream use by the LLM and Product teams. Ensure data quality, completeness, and ethical alignment.

### Goals per Dataset

#### 1. Submission Classification (AI Detection)
- QA and finalize 4000+ entries  
  - ~2,500 human submissions  
  - ~1,500 AI submissions  
- Tag subject domains and tools used  
- Prepare metadata and README for LLM handoff

#### 2. Feedback Annotation
- Finalize and QA ~1000 rubric-aligned samples  
  - At least 700 human samples  
  - At least 300 AI samples  
- Ensure rubric coverage across domains (min 3–5 disciplines)  
- QA annotation consistency and fill gaps in feedback formats  
- Document feedback pipeline and annotate examples clearly

#### 3. Revision Chain
- Finalize mapping and conversion of ~1000 real chains from RE3 / IteraTe  
- Generate and validate ~500 synthetic revision chains using prompt templates  
- QA structure (step order, author changes, timestamps, clarity of comments)  
- Finalize script documentation and update README with examples

### Sprint 2 Deliverables (Data Pillar)
- Final versions of all 3 datasets  
- QA reports and validation outputs  
- README + usage docs per dataset  
- Dataset-ready package for ingestion by the LLM team
