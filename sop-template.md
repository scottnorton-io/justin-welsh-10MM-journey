---
title: "SOP Title Goes Here"
filename: sop-template.md
version: 1.0
effective_date: YYYY-MM-DD
review_date: YYYY-MM-DD
owner: [Department or Role]
control_ids: ["CC-0.0", "CC-0.1"] # Replace with actual mappings
status: Draft
---

# 📘 [Insert SOP Title]

## 🧭 Purpose

Briefly explain **why** this SOP exists and what it ensures.  
Example: This SOP defines steps to securely onboard new employees and satisfy access control requirements.

---

## 🧱 Scope

Describe who and what this SOP applies to.  
Include systems, roles, processes, or departments as needed.

---

## 👥 Responsibilities

| Role              | Responsibility Description                            |
|-------------------|--------------------------------------------------------|
| Example: HR Admin | Sends initial access checklist                         |
| Example: IT Admin | Creates and revokes credentials                        |

---

## ⚙️ Procedure

### Step-by-Step Instructions

| Step | Who        | What                                                  | When            | Dependencies         | Notes                           |
|------|------------|-------------------------------------------------------|-----------------|----------------------|----------------------------------|
| 1    | Role Name  | Describe first task clearly and completely            | Trigger event   | Input/Precondition   | Additional clarifying info       |
| 2    | Role Name  | Next task...                                          | Timeline        | Dependencies         |                                  |
| ...  | ...        | ...                                                   | ...             | ...                  |                                  |

---

## 🔐 Control Mapping

This SOP contributes to meeting the following controls:

- `CC-#.#`: [Insert short control description]
- `CC-#.#`: [Optional second mapping]

Align this with `policy-to-control-map.csv` or `compliance-checklist.csv`.

---

## 🔄 Workflow Execution (Optional YAML Block)

To automate or simulate:

```yaml
workflow:
  name: [workflow_name_here]
  source: sop-template.md
  tasks:
    - step: "[Insert action]"
      assigned_to: "[Role]"
    - step: "[Next action]"
      assigned_to: "[Role]"
````

---

## 🎓 Training Mode Trigger (Optional)

> To simulate this SOP:
> “Run training simulation for \[SOP Title].”

This SOP supports assistant-led walk-through for onboarding, compliance training, or audits.

---

## 🔗 References

* `submission-log.csv` – Where to track actions
* `message-templates.md` – Communication/acknowledgment support
* `workflow-examples.md` – Task structure guide
* `user-personas.md` – Role definitions for formatting

---

## 🛑 Change Log

| Version | Date       | Changes             | Author       |
| ------- | ---------- | ------------------- | ------------ |
| 1.0     | YYYY-MM-DD | Initial SOP drafted | \[Your Name] |

---

## ✅ Assistant Usage Instructions

* To generate this template:

  > “Start a new SOP scaffold.”
* To insert into documentation set:

  > “Add this to sop-library-index.csv.”

---
