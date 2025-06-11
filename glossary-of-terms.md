 📚 Glossary of Terms

**Filename**: `glossary-of-terms.md`
**Version**: 1.0
**Last Updated**: 2025-06-11

---

## 🎯 Purpose

This glossary serves as a canonical reference for domain-specific, technical, and procedural terminology used throughout this project. The assistant uses this glossary to:

* Define terms in-context upon request
* Avoid inconsistent terminology across outputs
* Clarify acronyms and control names
* Improve accessibility for non-specialist audiences

When generating outputs, definitions should align exactly with the descriptions below unless otherwise stated.

---

## 🧾 Term Index

---

### **Access Control**

**Definition**: Mechanisms that regulate who can view or use resources in a computing environment. Includes both physical and logical controls.
**Usage Note**: Often mapped to `CC-1.1` or similar compliance controls.

---

### **Addendum**

**Definition**: A static file that expands the assistant’s knowledge base. Treated as immutable unless versioned and reuploaded.
**Usage Note**: Stored outside model memory. Examples: `training-manual.md`, `faq-repository.md`.

---

### **Audit Trail**

**Definition**: A chronological record of system activities that can be used to reconstruct and examine system or user activity.
**Usage Note**: Often cited as required evidence for monitoring controls.

---

### **Authentication**

**Definition**: The process of verifying the identity of a user or system.
**Types**: Single-factor, multi-factor (MFA/2FA).
**Related Controls**: `CC-1.2`, `CC-1.3`.

---

### **CIA Triad**

**Definition**: A foundational information security model composed of:

* **Confidentiality**: Preventing unauthorized access to data
* **Integrity**: Ensuring data is accurate and unaltered
* **Availability**: Ensuring systems/data are accessible when needed

---

### **Compliance Checklist**

**Definition**: A structured list of required controls used to assess or validate organizational adherence to a security framework.
**Source File**: `compliance-checklist.csv`

---

### **Control ID**

**Definition**: A unique identifier (e.g., `CC-2.1`) used to reference specific compliance controls or requirements in mappings, documents, or audits.

---

### **Evidence Submission**

**Definition**: The process of uploading or linking documentation that proves a control is implemented or a process followed.
**Example Fields**: `Submitted_By`, `Control_ID`, `Document_URL`, `Notes`

---

### **Gap Analysis**

**Definition**: A comparison process that identifies missing controls or documentation relative to a defined standard or checklist.
**Workflow Reference**: `workflow-examples.md` → “Compliance Gap Analysis”

---

### **Least Privilege**

**Definition**: A security principle that requires users to be given only the permissions necessary to perform their duties.
**Example**: A developer has read-only access to production logs but cannot modify them.

---

### **Markdown**

**Definition**: A lightweight markup language used to format documents for readability and structure.
**Usage**: Preferred output format for GPT responses unless otherwise specified.

---

### **Output History**

**Definition**: A structured ledger of all GPT-generated deliverables, tracked in `outputs-history.csv`.
**Fields**: `Timestamp`, `Output_Title`, `Input_Source`, `Filename`, etc.

---

### **Persona**

**Definition**: A user role model representing a category of stakeholders (e.g., Engineer, Compliance Manager).
**Reference File**: `user-personas.md`
**Usage Note**: Dictates tone, format, and content depth in assistant outputs.

---

### **SOP (Standard Operating Procedure)**

**Definition**: A detailed, written instruction used to achieve uniformity in the performance of a specific function.
**Structure**: Title, Purpose, Scope, Procedure Steps, Review Info

---

### **Static File System**

**Definition**: The environment in which this GPT assistant operates. It consists of a maximum of 20 static files (20MB max each) acting as the assistant’s extended memory.

---

### **Task Breakdown**

**Definition**: The conversion of a procedure or policy into discrete, actionable tasks.
**Workflow Reference**: `workflow-examples.md` → “SOP to Task Breakdown”

---

### **Template (Messaging)**

**Definition**: A reusable structure for communicating updates, changes, or policy rollouts.
**Examples**: Internal announcement, external compliance email
**Reference**: `message-templates.md`

---

### **Version Control (Documents)**

**Definition**: The practice of labeling and storing different versions of documents to track revisions over time.
**Naming Convention**: `filename_v1.md`, `filename_v2.1.md`

---

### **Weekly Summary Report**

**Definition**: A standardized document that provides high-level reporting of progress, blockers, and upcoming tasks.
**Reference**: `workflow-examples.md` → “Weekly Summary Report Generator”

---

## 🧠 Assistant Usage Instructions

* Match definitions exactly unless user provides override or context.
* Use glossary entries to clarify responses with embedded `(Definition: …)` on first use of uncommon terms.
* When requested, include full definitions inline or link to glossary section.

---
