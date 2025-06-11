# 🪪 Persona Prompt Guide

**Filename**: `persona-prompt-guide.md`  
**Version**: 1.0  
**Last Updated**: 2025-06-11

---

## 🎯 Purpose

This guide provides sample prompts mapped to the five primary user personas defined in `user-personas.md`. Each prompt is optimized to:

- Trigger relevant assistant workflows  
- Match tone and format expectations by role  
- Speed up common daily tasks or queries  

Use this guide to initiate structured outputs like SOPs, gap analyses, evidence generation, policy review, and summaries.

---

## 🧑‍💼 Compliance Manager

🎯 Goal: Evaluate evidence readiness, control coverage, audit posture

```text
- “Run a gap check for Q2 controls.”
- “Summarize which policies satisfy CC-4.1.”
- “List SOPs mapped to CC-10.1.”
- “Generate a weekly compliance summary report.”
- “Show all evidence submissions pending review.”
````

---

## 🧑‍💻 Technical Lead / Engineer

🎯 Goal: Implement and validate controls, write technical evidence

```text
- “Show me the script to validate TLS.”
- “List SOPs involving config changes.”
- “Validate this JSON payload against required fields.”
- “Create a Bash script to scan for exposed secrets.”
- “Generate technical evidence for CC-3.1 compliance.”
```

---

## 🧑‍💼 Executive Sponsor

🎯 Goal: Understand program status, risk posture, and high-level summaries

```text
- “Summarize this policy update for execs.”
- “Write a 5-bullet update on our PCI readiness.”
- “Explain what gaps we have and what’s blocked.”
- “Draft a leadership summary of our audit closure plan.”
- “Which SOPs matter most for our board-level risk exposure?”
```

---

## 🧑 Policy Owner / Document Creator

🎯 Goal: Write, update, or align documentation to controls

```text
- “Draft a data retention policy based on CC-9.1.”
- “Convert this SOP draft into a formatted checklist.”
- “Update the Acceptable Use Policy to meet CC-1.1.”
- “What controls does this procedure cover?”
- “Show me a reusable SOP template for onboarding.”
```

---

## 👩 External Assessor / Auditor

🎯 Goal: Review control alignment, evaluate artifacts, find gaps

```text
- “Summarize how this policy meets PCI DSS 3.4.1.”
- “List which controls are still unaccounted for.”
- “Generate a control-to-policy crosswalk.”
- “Is this screenshot sufficient for evidence under CC-3.2?”
- “What evidence supports our encryption implementation?”
```

---

## 📎 Usage Notes

* All prompts are valid in plain text — no special formatting required.

* You can prefix prompts with context:

  > “As a Policy Owner, draft…” or “For an assessor, generate…”

* These prompt styles activate workflows from:

  * `workflow-examples.md`
  * `training-manual.md`
  * `code-snippets-library.md`
  * `message-templates.md`

---
