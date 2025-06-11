# 🔄 Workflow Examples

**Filename**: `workflow-examples.md`
**Version**: 1.0
**Last Updated**: 2025-06-11

---

## 🎯 Purpose

This document defines structured, reusable workflow patterns that the GPT assistant can emulate or extend. These examples act as procedural templates for:

* Task execution
* Output structuring
* Process documentation
* SOP drafting

Each workflow includes a title, phase/stage breakdown, key inputs/outputs, and instructions for how the assistant should support or reproduce it.

---

## 📋 Workflow 1: Compliance Gap Analysis

**Use Case**: Identify gaps between documented policies and framework requirements (e.g., PCI DSS, SOC 2, ISO 27001).

### Phases:

1. **Collect Input**:

   * Addendums: `compliance-checklist.csv`, `training-manual.md`, `policy-library/`
2. **Cross-reference**:

   * Match each `Control_ID` with corresponding documentation.
3. **Evaluate Gaps**:

   * Flag `Status != Complete` or `Document_Reference` missing.
4. **Summarize**:

   * Create a gap report with columns: `Control_ID`, `Gap Reason`, `Suggested Action`.
5. **Output**:

   * Markdown or CSV-formatted gap summary for review.

---

## 🛠️ Workflow 2: SOP to Task Breakdown

**Use Case**: Convert a written SOP or policy into a task-oriented checklist or structured process model.

### Phases:

1. **Ingest SOP**:

   * Addendum: `training-manual.md` or similar
2. **Identify Actionable Steps**:

   * Use bullet structure or “Step X” formatting.
3. **Extract Task Objects**:

   * Create: `Step`, `Who`, `What`, `When`, `Dependencies`, `Notes`
4. **Format Output**:

   * Table or checklist with actionable descriptions.
5. **Optional**:

   * Export as JSON for automation or Notion import.

---

## ✉️ Workflow 3: Weekly Summary Report Generator

**Use Case**: Assemble a one-page summary of team actions or status updates from across documents.

### Inputs:

* `outputs-history.csv`
* Any daily logs, project plans, or recent deliverables.

### Steps:

1. Identify entries with `Date` in last 7 days.
2. Group by project/component or status (`Completed`, `In Progress`).
3. Highlight key accomplishments and deadlines.
4. Output a report with:

   * **Section 1**: Completed This Week
   * **Section 2**: Ongoing Tasks
   * **Section 3**: Blockers or Escalations
   * **Section 4**: Upcoming Due Dates

---

## 🧾 Workflow 4: Policy Mapping to Framework

**Use Case**: Map internal policy text to an external standard like PCI DSS v4.0 or ISO 27001.

### Phases:

1. **Select Target Standard**:

   * E.g., PCI DSS 3.2.1 → 4.0 crosswalk.
2. **Align Sections**:

   * Identify policy segments with keywords from requirement descriptions.
3. **Tag and Map**:

   * For each control: list `Policy_File`, `Section`, `Control_ID`.
4. **Create Matrix**:

   * Output format:
     \| Control\_ID | Covered? | Policy Name | Section | Notes |
5. **Flag Gaps**:

   * If no clear alignment, mark `Covered? = No`.

---

## 📘 Workflow 5: Narrative Generation from Structured Data

**Use Case**: Transform structured records into human-readable narratives (e.g., audit summaries, change logs).

### Inputs:

* `outputs-history.csv` or structured API JSON

### Steps:

1. Parse record fields (e.g., `Owner`, `Control_ID`, `Status`, `Date`).
2. Identify clusters or themes.
3. Apply template:

   > “On {{Date}}, {{Owner}} completed implementation of {{Control\_ID}}, which addressed {{Risk Area}}. This was logged in {{Document}} and is now marked as complete.”
4. Group outputs into paragraphs by time, theme, or team.

---

## 📂 Usage Tips for GPT Assistant

* When a user says “follow our process,” refer to this file.
* When unclear, suggest a starting workflow:

  > “Would you like me to follow the Compliance Gap Analysis or SOP Breakdown workflow?”
* Always output consistent headings and structure per example.
* Document any custom workflows initiated by user in `outputs-history.csv`.

---
