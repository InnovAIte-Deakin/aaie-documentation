# Software Requirements Specification (SRS)  
**AAIE – Data Curation and Generation**  
**Version:** 0.1 
**Date:** August 7, 2025  

---

## 1. Introduction  

### 1.1 Purpose  
This Software Requirements Specification (SRS) document outlines the functional and non-functional requirements for the Data Curation Pillar of the Artificial Assessment Intelligence for Educators (AAIE) project. The module enables team members to structure, validate, and manage a unified dataset that captures AI-assisted academic writing behavior across multiple domains.  

This includes rubric-based task prompts, AI and human interactions, and final student-like submissions categorized by quality. The system supports schema validation, peer and senior review workflows, and GitHub integration for version control. Future updates will include advanced metadata tagging, automation scripts for synthetic data generation, and visualization tools for dataset insights.  

### 1.2 Scope  
This system allows users to:  
- Structure and curate academic datasets for essay-style and short-answer assignments aligned with rubric-based prompts  
- Input and manage JSON records containing prompts, rubrics, LLM interactions, and multi-band student-style submissions  
- Validate dataset entries against a unified JSON schema  
- Run local validation scripts to detect common schema or content error  
- Flag and document missing fields such as rubric mismatches, incomplete submissions, or feedback gaps  
- Perform peer and senior reviews via GitHub Pull Requests  
- Organize data by academic domains for downstream use by the LLM development team  
- Track contributions and revisions using version control  
- Automate synthetic submission generation using prompt-controlled LLM pipelines  
- Utilize Continuous Integration (CI) tools for schema validation and PR-based dataset checks  
- Apply various weights rubric criteria for this version  

**Future enhancements for following trimesters:**  
- Expand dataset coverage to additional academic domains beyond the initial five  
- Increase the granularity of feedback types (e.g., rubric-aligned, holistic, inline comments)  
- Model multi-turn revision chains to reflect realistic student–LLM iterative interactions  
- Implement advanced metadata tagging for submission analysis and filtering  
- Curate and convert licensed public academic datasets into the AAIE unified schema format  
- Support for math, coding, and structured-answer assignments requiring non-essay LLM outputs  

### 1.3 Definitions, Acronyms, and Abbreviations  
- **AAIE**: Artificial Assessment Intelligence for Educators  
- **JSON**: JavaScript Object Notation  
- **CI**: Continuous Integration  
- **LLM**: Large Language Model  
- **PR**: Pull Request  
- **HD**: High Distinction (university grading band)  
- **GLO**: Graduate Learning Outcome  
- **API**: Application Programming Interface  
- **QA**: Quality Assurance  
- **CSV**: Comma-Separated Values  
- **Schema**: A defined structure that dataset entries must conform to  
- **Synthetic Submission**: A fictional student response generated via LLM prompts  

---

## 2. Overall Description  

### 2.1 Product Perspective  
The Data Curation Pillar is a foundational component of the AAIE project, supporting the creation of a unified, high-quality dataset for training and evaluating AI-assisted academic writing tools.  

It provides tools and workflows for contributors to create, validate, and manage structured JSON files that represent assignment prompts, rubrics, AI interaction chains, and multi-quality student-style submissions.  

It integrates with GitHub to support peer review, version control, and CI-based validation pipelines.  

Future iterations will include enriched revision chains, metadata layers, and deeper integration with licensed public datasets.  

### 2.2 User Needs  
- Clear contributor workflows for submitting curated JSON datasets and scripts  
- Schema validation tools to check for missing fields or structural errors  
- Dataset support for essay-style and short-answer academic tasks  
- Automation scripts for generating synthetic submissions based on prompts and rubrics  
- GitHub-based review process with support for peer and senior reviews  
- Ability to track validation status, submission quality bands, and domain coverage  
- CI pipeline to catch schema violations automatically on pull requests  
- Lightweight visualization/reporting of data coverage (future)  

### 2.3 Constraints  
- JSON schema structure must be strictly followed for all curated dataset files  
- Each JSON file must include at least 5 submissions covering quality bands from Excellent to Poor  
- Initial validation tools are CLI-based  
- All data must be contributed through version-controlled GitHub branches  
- Synthetic generation tools assume OpenAI-compatible API access  
- Reviewers must manually verify rubric-submission alignment and quality bands  
- Math or code-based assignments are out of scope for the current trimester  

### 2.4 Assumptions and Dependencies  
- Contributors are familiar with Git and GitHub workflows  
- Python 3.x environment is available  
- Submissions reflect realistic academic writing patterns  
- Initial dataset focuses on five domains (IT, Psychology, Engineering, Accounting, Teaching)  
- CI/validation tools rely on GitHub Actions setup  
- Prompt engineering produces believable, high-quality outputs  

---

## 3. System Features  

### 3.1 Load and Validate Dataset File  
**Description:** Validates JSON against schema.  
**User Story:** As a contributor, I want the system to validate my dataset file so I can meet project standards.  
**Acceptance Criteria:**  
- Confirms presence of all top-level fields  
- Rubric contains at least one criterion with 5 descriptors  
- Validates 5 distinct submissions across quality bands  
- Detects/report missing fields (e.g., llm_questions, feedback)  
- Returns clear error messages  

### 3.2 Normalize and Standardize Rubric Structure  
**Description:** Ensures rubrics follow consistent structure.  
**User Story:** As a contributor, I want to ensure rubrics are complete/consistent.  
**Acceptance Criteria:**  
- Each criterion has 5 bands  
- Non-empty descriptors  
- Labels match band names  
- Equal weighting assumed  

### 3.3 Generate Synthetic Submissions (Prompt-Based)  
**Description:** Generates realistic student-style responses.  
**Acceptance Criteria:**  
- At least one submission per band  
- Uses rubric wording  
- Select band + domain  
- Includes llm_questions/answers + final_submission  

### 3.4 Continuous Integration (CI) Validation on Push  
**Description:** Runs auto validation on PR.  
**Acceptance Criteria:**  
- Schema validation on each JSON  
- Flags malformed/missing fields  
- Rejects wrong folder structure  
- Logs validation errors in CI  

### 3.5 Peer and Senior Review Workflow  
**Description:** Supports structured reviews.  
**Acceptance Criteria:**  
- PR template requires rubric ID + domain  
- Tagging @peer-reviewer, @senior-reviewer  
- 2 peer + 1 senior approval before merge  
- Review checklist documented  

### 3.6 Schema Documentation Access  
**Description:** Provides human-readable schema.  
**Acceptance Criteria:**  
- schema_reference.md in repo  
- Example JSON in samples/  
- Linked in README  

### 3.7 Domain and Quality Coverage Reporting  
**Description:** Tracks domain coverage.  
**Acceptance Criteria:**  
- Counts rubrics + submissions per domain  
- Highlights missing quality bands  
- Export as CSV/JSON  

---

## 4. Future Work  

### 4.1 Multi-Turn Interaction Chains  
- Support multiple llm_question/answer pairs  
- Review guidelines for chains  
- Curation scripts extended  

### 4.2 Expanding Dataset Scope  
- Add code/math tasks  
- New rubrics for STEM  
- Expand domains (Law, Finance, Env. Science)  

### 4.3 Advanced Feedback Variants  
- Rubric-aligned  
- Holistic  
- Inline comments  

### 4.4 Licensed Public Dataset Conversion  
- Map datasets to schema  
- Rebuild rubrics  
- Ensure band coverage  

### 4.5 Domain & Coverage Reporting Tools  
- Count rubrics per domain  
- Highlight missing bands  
- Export reports  

---

## 5. External Interface Requirements  

### 5.1 User Interface  
- **CLI**: Run validation.py & generation scripts locally  
- **GitHub**: PR workflow, CI logs, docs in Markdown  
- **Optional Utilities**: Notebooks/scripts for reporting  

### 5.2 Software Interfaces  
- Python 3.x validation/generation scripts  
- JSON schema validation (jsonschema library)  
- GitHub Actions CI  
- OpenAI API for synthetic generation  

---

## 6. Non-Functional Requirements  

### 6.1 Performance  
- Validation <5s per file  
- CI <2m per PR  
- Dashboard <3s for <100 files  

### 6.2 Usability  
- Clear contributor instructions  
- Human-readable validation errors  
- PR templates with rubric IDs  

### 6.3 Reliability  
- Schema validation must catch errors  
- Reviews prevent invalid merges  
- LLM outputs checked  

### 6.4 Maintainability  
- Schema versioned  
- Scripts follow coding standards  
- GitHub workflow enforced  

### 6.5 Scalability  
- Support 50 → 500+ files  
- Modular dashboards/pipelines  
- Expand domains without refactoring core  

### 6.6 Data Integrity & Security  
- Git version control for history  
- Restricted push access  
- CI ensures valid files  

---

## 7. Appendices  

### 7.1 Glossary  
- **AAIE**: AI for Educators project  
- **Rubric**: Scoring guide with multiple criteria and levels  
- **JSON**: Data format used for files  
- **Validation**: Schema compliance check  
- **Schema**: Required file structure  
- **LLM**: Large Language Model  
- **Synthetic Submission**: AI-generated student-like response  
- **Quality Band**: Excellent → Poor scale  
- **Prompt Engineering**: Crafting inputs to guide LLMs  
- **Peer Review**: Review by teammates  
- **CI**: Continuous Integration pipeline  
- **Revision Chain**: Iterative AI-student exchanges  
- **Domain**: Academic subject area  

---

## 8. References  
- [Python Official Documentation](https://docs.python.org/3/)  
- [JSON Schema Specification](https://json-schema.org/)  
- [jsonschema (Python Library)](https://python-jsonschema.readthedocs.io/)  
- [GitHub Docs: Pull Requests](https://docs.github.com/en/pull-requests)  
- [GitHub Actions Documentation](https://docs.github.com/en/actions)  
- [OpenAI API Reference](https://platform.openai.com/docs/api-reference)  
- [Prompt Engineering Guide](https://github.com/dair-ai/Prompt-Engineering-Guide)  
- [Markdown Guide](https://www.markdownguide.org/)  
- [PEP8 Python Style Guide](https://peps.python.org/pep-0008/)  
- [Visual Studio Code (VSCode)](https://code.visualstudio.com/)  
- [Git Documentation](https://git-scm.com/doc)  
- [JSON Formatter & Validator](https://jsonlint.com/)  
- [Creative Commons License Directory](https://creativecommons.org/about/cclicenses/)  
