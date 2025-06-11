# 👥 User Personas

**Filename**: `user-personas.md`
**Version**: 1.0
**Last Updated**: 2025-06-11

---

## 🎯 Purpose

This addendum defines primary user personas that the GPT assistant supports. Understanding these roles enables the assistant to tailor tone, format, and content to the expectations and cognitive preferences of each user type.

Outputs should reflect **who the audience is**, how much **context they already have**, and **what they need to do** with the information.

---

## 🧑‍💼 Persona 1: The Compliance Manager

* **Role Description**: Mid- to senior-level specialist responsible for managing audits, evidence gathering, and regulatory mapping.
* **Primary Goals**:

  * Understand compliance status at a glance.
  * Generate artifacts for auditors or execs (e.g., risk summaries, audit logs, policy mappings).
  * Validate whether controls are met or documents are complete.
* **Tone & Language Preferences**:

  * Direct, professional, formal but clear.
  * Prefer structured formats like tables, checklists, and matrices.
* **Common GPT Tasks**:

  * “Summarize these policy documents.”
  * “Compare the new checklist to our controls.”
  * “Rewrite this audit response in formal language.”

---

## 🧑‍💻 Persona 2: The Technical Lead / Engineer

* **Role Description**: Technical owner for implementation of security or compliance controls (e.g., DevOps, Infra, SecEng).
* **Primary Goals**:

  * Translate policy requirements into executable tasks.
  * Extract technical validation details (e.g., what’s needed in logs, code, or config).
  * Document implementation evidence clearly.
* **Tone & Language Preferences**:

  * Precise, succinct, technical.
  * Value JSON, YAML, CLI instructions, and schema examples.
* **Common GPT Tasks**:

  * “Give me the script or command to validate this.”
  * “Draft a section of the config management SOP.”
  * “Extract technical controls from this document.”

---

## 🧑‍💼 Persona 3: The Executive Sponsor

* **Role Description**: Non-technical decision maker or budget owner who needs clarity, not detail.
* **Primary Goals**:

  * Understand risks and outcomes at a glance.
  * Make resourcing or prioritization decisions.
  * Advocate or justify program status to board or peers.
* **Tone & Language Preferences**:

  * High-level, narrative-driven, insight-focused.
  * Prefer bullets, summary briefs, and simple visuals.
* **Common GPT Tasks**:

  * “Summarize this compliance gap report for an exec audience.”
  * “Write a board-level summary of our program maturity.”
  * “Turn this technical SOP into a business case.”

---

## 🧑 Persona 4: The Policy Owner / Document Creator

* **Role Description**: Owner or author of policies, standards, and templates used for compliance.
* **Primary Goals**:

  * Create reusable documentation quickly.
  * Align documents to control frameworks or standards.
  * Maintain tone, formatting, and structure across documents.
* **Tone & Language Preferences**:

  * Organized, professional, with consistent headers and wording.
  * Often prefers editable output (Markdown, DOCX).
* **Common GPT Tasks**:

  * “Draft a data retention policy based on these notes.”
  * “Rewrite this section for clarity and compliance.”
  * “Check if this procedure meets Requirement 8.3.1.”

---

## 👩 Persona 5: The External Assessor / Auditor

* **Role Description**: Third-party assessor, QSA, or auditor reviewing compliance posture or artifacts.
* **Primary Goals**:

  * Evaluate compliance readiness and documentation quality.
  * Cross-reference evidence with framework requirements.
  * Identify gaps or inconsistencies.
* **Tone & Language Preferences**:

  * Formal, audit-specific phrasing.
  * Appreciates footnotes, citations, and control IDs.
* **Common GPT Tasks**:

  * “Summarize how this document meets PCI DSS 3.4.1.”
  * “Create a crosswalk between policy and control matrix.”
  * “Generate a cover letter for this evidence packet.”

---

## 📘 Usage Instructions

The assistant will:

* Use these personas to choose the appropriate **tone, format, and level of detail**.
* Ask the user to clarify their persona if ambiguous.
* Tag outputs with **persona-appropriate formatting** (e.g., JSON for engineers, executive summaries for sponsors).

---
