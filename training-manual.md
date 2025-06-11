# 📘 Training Manual

**Filename**: `training-manual.md`  
**Version**: 2.0  
**Last Updated**: 2025-06-11

---

## 🎯 Purpose

This manual provides training and operational guidance for executing key SOPs. It is formatted for:

- Assistant-led training simulations  
- Notion or JSON-based task ingestion  
- Compliance traceability and control alignment  

All procedures support modular reuse across compliance, onboarding, and IT operations.

---

## 🧠 Key Training Concepts

### 1. 📚 Understanding Compliance Roles

- **Compliance Manager**: Oversees evidence collection, policy enforcement  
- **Policy Owner**: Maintains documentation and alignment  
- **Technical Operator**: Implements and validates controls  
- **Auditor/Assessor**: Evaluates compliance posture  

→ See `user-personas.md` for persona-specific formatting:contentReference[oaicite:0]{index=0}.

---

### 2. 🔒 Security and Compliance Foundations

- **CIA Triad**: Confidentiality, Integrity, Availability  
- **Access Models**: Role-Based, Least Privilege  
- **Documentation Types**:
  - Policies = Intent  
  - Standards = Rules  
  - Procedures = How  
  - Guidelines = Suggestions  

---

### 3. 📋 Document Management Practices

- Versioning: `policyname_v1.2.md`  
- Approval Metadata: `Effective Date`, `Approved By`, `Version`  
- Storage: Access-controlled, central repository  
- Review: Annual or upon control update  

---

## ✅ SOP: Onboarding a New Team Member

**Objective**: Ensure all systems, training, and documentation are completed during employee onboarding.

### Task Breakdown

| Step | Who          | What                                                   | When              | Dependencies           | Notes                                 |
|------|---------------|--------------------------------------------------------|-------------------|------------------------|----------------------------------------|
| 1    | HR            | Complete intake form                                   | Day 0             | Offer letter signed    | May include background verification    |
| 2    | IT Admin      | Provision credentials and system access                | Day 1             | Intake form            | Use secure channel                     |
| 3    | Team Manager  | Assign training modules (e.g., Security 101)           | First week        | Account provisioned     | Use LMS or internal tracker            |
| 4    | Ops/Manager   | Share AUP, Code of Conduct, SOPs                       | First week        | Email enabled          | Use secure document delivery platform  |
| 5    | New Hire      | Confirm policy acknowledgment                          | Within 7 days     | Documents shared       | e-signature or form tracking           |
| 6    | Manager       | Schedule and complete 30-day check-in                  | Day 30            | Onboarding complete    | Confirm confidence + clarity           |

**Relevant Controls**: `CC-1.1`, `CC-2.2`, `CC-5.1`

### 🔄 Workflow Execution

```yaml
workflow:
  name: onboarding_checklist
  source: training-manual.md
  tasks:
    - step: "Complete HR intake form"
      assigned_to: "HR"
    - step: "Provision access"
      assigned_to: "IT Admin"
    - step: "Assign training"
      assigned_to: "Manager"
    - step: "Distribute policy documents"
      assigned_to: "Ops"
    - step: "Confirm acknowledgment"
      assigned_to: "New Hire"
    - step: "30-day check-in"
      assigned_to: "Manager"
