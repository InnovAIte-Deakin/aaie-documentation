# DEPRECATED: Data Curation & Generation Pillar Team

> **This document is archived**  
> The plans and documentation below reflect early work done **prior to the establishment of the unified AAIE dataset structure**.  
> This is preserved for historical context only. The most up-to-date plans, schemas, and pipeline documentation can be found in the upstream [`aaie-documentation`](https://github.com/InnovAIte-Deakin/aaie-documentation) repository.

---

## Overview, Goals, and Objectives

The **Data Curation & Generation Pillar** supported the AAIE project by developing scalable, ethics-safe datasets to train and evaluate large language models (LLMs) for educational assessment. This included data for:

- AI-generated content detection
- Rubric-aligned feedback engines

Our goal was to create reproducible, high-quality datasets and processing pipelines for future use by modelling and product teams.

---

## Aims for Trimester

- Collect and curate **1000+ academic prompts and rubrics** from public sources  
- Generate **synthetic student submissions** using GenAI and human-written samples  
- Annotate **1000+ submissions** with feedback and rubric-aligned grading  
- Build **500+ prompt revision chains** (prompt → AI draft → edits → final)  
- Deliver a documented, ethics-compliant pipeline for dataset processing and validation  

---

## Deliverables

### General (Shared by Both Subprojects)

- Python-based data processing pipeline (reproducible)
- JSON/CSV schema definitions
- Folder structure, naming conventions, and metadata templates
- Ethics and licensing protocol draft
- Automated QA tools (rubric alignment, duplication check, formatting)

---

### AI Detection Dataset (Classifier)

- 1000+ synthetic submissions  
  - 350 AI-generated  
  - 300 human-style  
  - 350 hybrid  
- 500+ revision chains (from prompt to final submission)
- Use case: detect invisible AI usage, model revision behavior

---

### Feedback Generation Dataset

- 500+ rubric + prompt pairs
- 1000+ annotated submissions  
  - Grades, feedback comments, rubric-criterion match
- Use case: train feedback generation and rubric alignment models

---

## Long-Term Deliverables

- Expansion to **other data types** (e.g., code, math, reports)
- Further refinement of:
  - QA tools
  - Ethics documentation
  - Dataset coverage
- Integration with **LMS tools** and modelling pipelines
- Reusable **annotation guides** and **benchmark evaluation sets**
- Automated **PII detection**
- Dataset **governance process** for future onboarding

---

*Original work completed prior to GitHub setup. Now deprecated in favor of unified dataset contributions.*
