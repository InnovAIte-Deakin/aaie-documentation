# LLM Team Meeting Takeaways  
**Date:** 1 August 2025  

---

## 1. Project Execution Structure & Sprint Transition  
- **Sprint 1** concludes this week; planning for **Sprint 2** begins.  
- Over the weekend (Saturday–Sunday), each member will conduct focused research on their assigned task and submit a **1-page bullet-point summary** by Monday for review with Nebula.  
- **Sprint 2** will initiate **formal implementation** using the revised team structure and planner tasks.  

---

## 2. Revised Task Breakdown and Team Allocation  
This sprint’s roles include:  
- **Prompt Engineering:** Designing effective few-shot prompts based on sample submissions and rubrics.  
- **Model Exploration & Benchmarking:** Testing lightweight models (TinyLLaMA, NanoGPT) and APIs (OpenAI, Google AI Studio).  
- **Evaluation:** Designing performance metrics to assess output quality and rubric alignment.  

**Final structure:**  
- Prompt + Model Team: **7 members**  
- Evaluation Team: **3 members**  
- Leadership assigned to both tracks.  

---

## 3. Prompt Engineering Approach  
- Prompt engineering is now the **central strategy** — PO does not want fine-tuning.  
- Members will use **synthetic data** from the data team for testing.  

---

## 4. Model Strategy and Selection Discussion  
- Pair **prompt engineering** with **lightweight LLMs** for cost-effective deployment.  

**Proposed models:**  
- **TinyLLaMA:** Few-shot learning; lacks predefined tokenization.  
- **Qwen:** Previously explored for fine-tuning.  
- **Mistral, Gemma, Phi:** Open-source models for HuggingFace-based prompt engineering.  
- **Claude, Gemini, OpenAI API:** Low-cost/free trial options for immediate prototyping.  

**Tasks:**  
- Compare usability, performance, and cost.  
- Use **HuggingFace + Google Colab** for testing/prototyping.  

---

## 5. Evaluation Metrics and Output Validation  
- Evaluation team to define **objective performance metrics** for both detection and feedback.  

**Suggested metrics:**  
- **Detection:** Accuracy of AI vs human classification.  
- **Feedback:** Rubric alignment, coherence of generated feedback.  

Metrics will be **documented and refined** iteratively.  

---

## 6. Documentation Strategy  
- No standalone documentation team — **all members** document their own work.  
- One member per subteam (Prompt/Model + Evaluation) responsible for:  
  - Updating **solution architecture**  
  - Maintaining **Markdown docs** in GitHub via PR workflow  
- **Architecture updates** required per PO feedback.  

---

## 7. Use of APIs and Technical Tools  
- APIs not initial focus; deferred unless deployment requires it.  
- Current focus: **local + Colab-based experiments** using:  
  - HuggingFace pipelines  
  - Google AI Studio (Gemini APIs)  
  - Claude & OpenAI trial tokens  

---

## 8. Final Team Distribution & Leadership  
- Members self-selected into teams.  
- Leadership:  
  - **Two leads** for Prompt + Model Team  
  - **One lead** for Evaluation Team  
- Leaders to coordinate **task breakdown, GitHub PR flow, weekly deliverables**.  

---

## 9. GitHub Workflow & Documentation Process  

**Central Source of Truth:**  
- GitHub = single source for code, prompts, models, evaluation outputs.  

**Branching Strategy:**  
- All PRs → **development branch**.  
- Final merge into **main** after Nebula’s approval.  

**Pull Request Requirements:**  
1. Link PR to a Planner card.  
2. 2 peer reviews → 1 senior leader review → Nebula review.  

**Review Expectations:**  
- Turnaround: **max 2 days**.  
- Each member: **2+ peer reviews** per sprint.  

**Documentation Format:**  
- All planning/research/technical work as `.md` files.  
- **Clarification pending** from Khushi on Netlify deployment via Astro.  
- Contributors must **verify Netlify previews** before merging.  

---

## 10. Action Plan and Next Steps  

| Task | Owner | Deadline |  
|------|-------|----------|  
| 1-page research summary on assigned task | All members | Monday |  
| Update architecture diagram (new strategy) | Assigned Documentation Members | Next Sprint |  
| Evaluate models with test prompts | Prompt/Model Team | Next week |  
| Develop evaluation rubric + testing plan | Evaluation Team | Next week |  

---
