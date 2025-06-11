Here is the detailed content for the addendum file **`project-overview.md`**:

---

# 📘 Project Overview

**Filename**: `project-overview.md`
**Last Updated**: 2025-06-11
**Version**: 1.0

---

## 🎯 Purpose

This document serves as the definitive reference for the scope, goals, and operational context of the project supported by the GPT assistant. It provides a high-level narrative that orients both AI and human collaborators around shared objectives and constraints.

---

## 🧭 Project Summary

This project establishes a **modular GPT assistant** configured to operate within a **static, flat file environment** of up to 20 files (each ≤20MB). The assistant performs structured tasks, synthesizes knowledge, and supports project execution by reading from and writing based on these modular memory units (“addendums”).

It is not a chatbot — it is a **synthetic work assistant** trained to execute mission-critical tasks with reliability and repeatability.

---

## 📌 Primary Goals

1. **Operationalize AI** in environments where internet access, real-time APIs, or persistent memory are restricted or undesired.
2. **Enable structured workflows** using static file formats (Markdown, CSV, JSON, DOCX, TXT).
3. **Support extended reasoning** by coordinating across documents to simulate continuity and domain understanding.
4. **Allow scalable use cases**, such as policy analysis, compliance drafting, training content creation, and task execution without dependency on conversational memory.

---

## 🔑 Key Functional Areas

| Function                 | Description                                                               |
| ------------------------ | ------------------------------------------------------------------------- |
| Content Analysis         | Summarize, compare, extract, and reformat document content.               |
| Instruction Execution    | Perform repeatable tasks such as writing procedures or validating inputs. |
| Document Synthesis       | Merge multiple files into structured summaries, briefs, or narratives.    |
| File Emulated Memory     | Simulate continuity using filenames, headers, and structure.              |
| Contextual Task Modeling | Apply best practices based on role/persona models stored in addendums.    |

---

## 👥 Stakeholders

| Role          | Name/Org (Optional)  | Responsibilities                                         |
| ------------- | -------------------- | -------------------------------------------------------- |
| Owner         | \[User/Org]          | Sets vision, provides files, approves outputs            |
| GPT Assistant | `gpt-assistant-core` | Executes tasks, simulates continuity, performs synthesis |
| Contributors  | \[TBD]               | Provide files or updates to addendums                    |

---

## 🗃️ Addendum Ecosystem (Connected Files)

This assistant relies on a supporting set of addendum files. See `llms.txt` for definitions and operational policy. Examples include:

* `tone-and-style-guide.md` – Sets brand tone and language rules.
* `compliance-checklist.csv` – Supplies standards or checklist items.
* `workflow-examples.md` – Provides models for output structure.
* `glossary-of-terms.md` – Clarifies technical language used in outputs.

---

## ⚙️ Execution Guidelines

1. **Requests should be task-specific.** Example: “Summarize the SOP in training-manual.md.”
2. **Assistant can reference multiple files at once.** Example: “Compare outputs-history.csv and training-manual.md.”
3. **User must simulate memory.** This is done by uploading relevant files each time or naming them explicitly in prompts.
4. **Outputs are meant to be modular and reusable.** The assistant defaults to formats like Markdown, bullet lists, or JSON.

---

## 📅 Milestones & Phases

| Phase   | Description                                                            |
| ------- | ---------------------------------------------------------------------- |
| Phase 1 | Deployment of assistant and upload of baseline addendums               |
| Phase 2 | Task execution: summaries, gap analyses, SOP conversions, etc.         |
| Phase 3 | Expansion to multi-role, multi-domain tasks as addendums evolve        |
| Phase 4 | Finalization of exportable playbooks and modular AI-assisted documents |

---

## ✅ Success Criteria

* Assistant produces human-grade outputs in under 2 iterations per prompt.
* Outputs reference and cite supporting files consistently.
* New team members can onboard using GPT + project files alone.
* Project scope expands to support multiple departments or verticals.

---

## 🔒 Boundaries and Limitations

* No persistent memory — all continuity is simulated through files.
* No online access — everything must be file-based.
* No hallucination — assistant must reference sources explicitly or request them.

---

## 📬 Contact and Support

* GPT Implementation Lead: *\[Your Name or Handle]*
* File Stewardship: *\[Optional admin role for keeping addendums updated]*

---
