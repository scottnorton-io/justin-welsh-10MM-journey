# 📖 FAQ Repository

**Filename**: `faq-repository.md`
**Version**: 1.0
**Last Updated**: 2025-06-11

---

## 🎯 Purpose

This addendum functions as a living archive of the most common questions and requests encountered in the project. The assistant will reference this file when:

* Similar queries are submitted repeatedly.
* A templated or prior-approved answer exists.
* Users ask, “What should I ask?” or “How do I do X?”

The assistant may also propose question rewordings based on this repository.

---

## 🧩 Structure

Each entry includes:

* **Question**: Commonly asked phrasing
* **Intent**: What the user is trying to accomplish
* **Answer**: The standardized or previously approved output
* **Addendums to Reference**: Supporting files for deeper analysis or sourcing
* **Tags**: Quick categorization for future retrieval

---

## 📝 FAQ Entries

---

### **Q1: How do I know if a policy satisfies a compliance requirement?**

* **Intent**: Validate if a document addresses a control
* **Answer**:
  To determine if a policy satisfies a compliance requirement, cross-reference its content against the control's language in `compliance-checklist.csv`. Look for evidence of:

  * Direct alignment with requirement text
  * Defined responsibilities
  * Enforceable actions
  * Review dates and ownership
    If any of these are missing, it may only partially satisfy the requirement. Use `workflow-examples.md` → "Policy Mapping to Framework" for step-by-step support.
* **Addendums to Reference**: `compliance-checklist.csv`, `workflow-examples.md`
* **Tags**: `compliance`, `policy review`, `mapping`

---

### **Q2: Can you summarize this document for an executive audience?**

* **Intent**: Create a high-level, non-technical briefing
* **Answer**:
  Absolutely. For executive summaries:

  * Use plain language and minimize jargon
  * Focus on outcomes, not process
  * Emphasize risk, opportunity, and status
  * Limit to 3–5 bullet points or a brief paragraph
    Include: purpose, result, impact, next steps.
* **Addendums to Reference**: `tone-and-style-guide.md`, `user-personas.md` (Executive Sponsor)
* **Tags**: `executive summary`, `tone`, `document transformation`

---

### **Q3: What should I include in a standard operating procedure (SOP)?**

* **Intent**: Draft or validate an SOP template
* **Answer**:
  Every SOP should include:

  * **Title and Version**
  * **Purpose**
  * **Scope**
  * **Responsibilities**
  * **Procedural Steps**
  * **References or Links**
  * **Review/Approval Metadata**
    Refer to `training-manual.md` for example structures.
* **Addendums to Reference**: `training-manual.md`, `tone-and-style-guide.md`
* **Tags**: `sop`, `documentation`, `templates`

---

### **Q4: How should I cite a file or document in my output?**

* **Intent**: Clarify citation format for file references
* **Answer**:
  Use the following citation format for in-line references:
  `【filename.txt†L12-L20】` for line-based docs or
  `【filename.pdf†Section 2.1】` for structured PDFs.
  Always include the filename and section details for traceability.
* **Addendums to Reference**: `tone-and-style-guide.md`, `project-overview.md`
* **Tags**: `citation`, `output formatting`, `file references`

---

### **Q5: What’s the best format for a weekly status summary?**

* **Intent**: Create a standardized report structure
* **Answer**:
  Weekly summaries should include:

  * ✅ Completed Tasks
  * 🕗 In Progress
  * ⚠️ Blockers / Risks
  * 📅 Upcoming Deadlines
    Use Markdown with clear headings and bullet lists. See example in `workflow-examples.md`.
* **Addendums to Reference**: `workflow-examples.md`, `tone-and-style-guide.md`
* **Tags**: `reporting`, `weekly summary`, `markdown`

---

### **Q6: What should I upload for a compliance review?**

* **Intent**: Prepare supporting evidence for audit readiness
* **Answer**:
  Upload the following where applicable:

  * Policies (e.g., Acceptable Use, Data Classification)
  * Logs or screenshots of technical control implementation
  * Evidence of approval (sign-off records)
  * Training acknowledgments
  * Change tickets or summaries
    Each document should correspond to a `Control_ID` in `compliance-checklist.csv`.
* **Addendums to Reference**: `compliance-checklist.csv`, `training-manual.md`
* **Tags**: `compliance evidence`, `audit`, `control matching`

---

## 🔄 Assistant Instructions

* If a prompt closely matches an entry, **reuse the answer** and update references/context.
* If a user seems unclear, suggest asking one of these preloaded questions.
* When building new FAQs based on repeated prompts, append them here in the same format.

---
