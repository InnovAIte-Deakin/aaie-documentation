# GitHub Workflow Document

## Official Contribution Process for T2 2025 and Beyond

This GitHub structure has been established as the standard for all teams working on the  
AAIE project, both for the current trimester (T2 2025) and for future trimesters. It is  
designed to ensure a clean, conflict-free development environment, support collaborative  
workflows, and maintain high code quality across all contributions.  

All contributors and leads must follow the structure outlined below.  

---

## 1. Repository Structure & Branching Policy
- The **main** branch will remain empty and protected, only accessible by **Nebula Alam**.  
- All development work will be integrated into the **development** branch.  
- Only the mentor (Nebula Alam) has merge access to **development**.  
- The **main** branch will be synced with **development** at defined milestones (e.g., mid-trimester and final release).  

---

## 2. Folder Structure Setup
- Each Team Lead is responsible for defining and managing the folder structure relevant to their domain or task (e.g., Prompt Engineering, Data Curation, Model Training).  
- Before any work begins, submit a PR containing **only the folder structure**.  
- No code or documentation files should be included.  
- This PR will be fast-tracked for mentor approval.  

---

## 3. Contributor Workflow
All contributors must follow these steps:

1. **Fork the full repository from your team’s development branch**  
   Ensure you fork the entire repository, not just the main branch.  

2. **Create a local feature branch in your fork**  
   - Name it clearly (e.g., `feature/model-evaluation`, `feature/interface-design`).  

3. **Complete your work locally**  
   - Follow the folder structure defined by your team lead  
   - Ensure all file names, content, and locations are relevant and organized  

4. **Submit a Pull Request (PR)**  
   - **Base**: `development` branch of the main repo  
   - **Compare**: your feature branch from your fork  
   - Add a meaningful title and description explaining your changes  

---

### When to Use One PR for Multiple Files
Use **one PR** when the changes:  
1. Belong to the same task/feature.  
   - Example: Adding a new feature like “User Login” might involve `login.js`, `authController.py`, and `README.md`.  
   - Since they all relate to the same feature, they should go in one PR.  

2. Depend on each other.  
   - Example: Updating database schema + updating the code that uses that schema.  
   - If you split them into separate PRs, one will fail without the other.  

---

### When to Use Multiple PRs
Use **separate PRs** when:  
1. Changes are unrelated.  
   - Example: Fixing a typo in `README.md` and refactoring code in `app.py`.  
   - Reviewers may not want to review documentation changes together with logic changes.  

2. Different reviewers are responsible.  
   - Example: Frontend team reviews UI (`style.css`, `index.html`) while Backend team reviews APIs (`api.js`, `server.py`).  
   - Easier to split PRs for each group.  

3. Risk of blocking progress.  
   - Example: You have a large feature but also a small bug fix.  
   - If you bundle both in one PR and the feature needs more discussion, the bug fix is delayed unnecessarily.  

---

### Best Practices
- Small, focused PRs are better — easier to review, test, and approve.  
- Group related changes together in one PR.  
- Split into multiple PRs if the changes are too large, unrelated, or need different reviewers.  
- For any **diagram updates**, save the diagram as a **PNG file**.  
  - Alongside the diagram, create or update a **Markdown (.md)** file that links to the PNG.  
  - This keeps documentation clean and ensures diagrams are viewable directly from GitHub.  

---

## 4. Review & Merge Process
Before any PR is merged:  
- It must be reviewed and approved by:  
  - **2 peers** from your team  
  - **1 senior reviewer** (team lead or project lead)  

- Final approval and merge will be completed by the mentor (**Nebula Alam**).  

---

## 5. General Guidelines
- Do **not** submit pull requests to the `main` branch — this is strictly prohibited.  
- If unsure about the process, reach out to your team lead for support.  
- All work must follow this structure — no exceptions.  

This structure will be enforced throughout the trimester to ensure a clean, transparent, and  
collaborative development process. Following this standard will help prevent merge  
conflicts, improve traceability, and allow future teams to build on a reliable foundation.  

---

## 6. Reviewing PR Template
Use the following template for all reviews:  

```markdown
## Summary
- (What & why)

## Issue Reference
- If any

## Type
- [ ] feat
- [ ] fix
- [ ] refactor
- [ ] docs
- [ ] test
- [ ] chore

## Changes
- Bullet the key changes

## Screenshots/Logs
- (If UI/logs are relevant)

## How to Test (If Relevant)
- Steps or commands

## Risk & Rollback (If Relevant)
- Risk level: Low/Med/High
- Rollback plan:

## Reviewers
- Peers: @<name>, @<name>
- Senior: @<name>

---

⚠️ **Caution**  
All reviews must be completed carefully and according to the required format.  
Incomplete, careless, or missing reviews will not be accepted and may result in penalties.  
Please take the time to review thoroughly and provide constructive, well-justified feedback.
