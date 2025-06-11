# 🧠 Training Scenarios

**Filename**: `training-scenarios.md`  
**Version**: 1.0  
**Last Updated**: 2025-06-11

---

## 🎯 Purpose

This file defines assistant-powered walkthroughs of key SOPs in “Training Mode.” Each scenario is role-specific and simulates a sequence of assistant/user interactions to reinforce procedural understanding and compliance readiness.

These can be used for:
- Internal onboarding
- SOP rehearsal before an audit
- Hands-on role-based simulations
- LMS integrations or assistant live training

---

## 🔄 Scenario: `onboarding_simulation`

**Role**: IT Admin  
**SOP**: Onboarding a New Team Member  
**Source**: `training-manual.md` → Onboarding SOP:contentReference[oaicite:0]{index=0}

```yaml
scenario: onboarding_simulation
role: IT Admin
steps:
  - prompt: "What should I do first?"
    reply: "Check that HR has completed the intake form for the new hire."
  - prompt: "Why is that required?"
    reply: "Access credentials must be provisioned based on verified HR authorization."
  - prompt: "Ok, the form is complete — what next?"
    reply: "Provision the new hire's system credentials — email, VPN, and core tools."
  - prompt: "How do I share those credentials securely?"
    reply: "Use the company-approved password manager invite or encrypted delivery channel."
  - prompt: "What do I do after that?"
    reply: "Confirm that training modules are assigned and documentation has been sent by the manager."
````

---

## 🔄 Scenario: `offboarding_simulation`

**Role**: Compliance Officer
**SOP**: Offboarding a Departing Team Member
**Source**: `training-manual.md` → Offboarding SOP

```yaml
scenario: offboarding_simulation
role: Compliance Officer
steps:
  - prompt: "Where should I begin?"
    reply: "Start by confirming that HR has received formal departure notification from the manager."
  - prompt: "That’s confirmed — what now?"
    reply: "Ensure IT has scheduled credential revocation for the employee’s final day."
  - prompt: "Do I need to do anything else?"
    reply: "Yes — ensure documentation handoff is complete and the employee has no lingering access to shared folders or email."
  - prompt: "What do I use to track that?"
    reply: "Use the Offboarding Checklist and Asset Return Form documented in `training-manual.md` and log everything in `submission-log.csv`."
```

---

## 🔄 Scenario: `policy-review_simulation`

**Role**: Policy Owner
**SOP**: Performing an Internal Policy Review
**Source**: `training-manual.md` → Policy Review SOP

```yaml
scenario: policy-review_simulation
role: Policy Owner
steps:
  - prompt: "Where do I start?"
    reply: "Open the latest version of the policy and check for metadata completeness — title, version, effective date."
  - prompt: "What if it’s missing a review date?"
    reply: "You’ll need to insert a new `Review Date` field and set a reminder for annual reassessment."
  - prompt: "How do I check if this policy still aligns with controls?"
    reply: "Cross-reference it against relevant Control_IDs in `compliance-checklist.csv` and `policy-to-control-map.csv`."
  - prompt: "Ok, I've edited it — what next?"
    reply: "Submit the updated version for sign-off using your internal approval workflow. Once approved, update the file and notify relevant teams."
```

---

## 🧪 Usage Instructions

* Trigger Training Mode with:

  > “Run training simulation for onboarding as \[Role].”

* Use prompt-response sequences to:

  * Simulate assistant coaching
  * Reinforce procedural memory
  * Drive checklist completions

* Optional:

  * Extend each scenario into a branching dialogue
  * Assign “quizzes” for LMS scoring or tracking

---

Here are **three additional Training Mode scenarios** to expand your SOP simulation suite:

* ✅ Evidence submission (Compliance Manager)
* 🔐 Access revocation (IT Admin)
* 🚨 Incident response (Security Engineer)

These align with your documented SOPs and control mappings, and follow the same structured YAML prompt-response format for assistant-guided training.

---

## 🔄 Scenario: `evidence_submission_simulation`

**Role**: Compliance Manager
**SOP**: Submitting Compliance Evidence
**Source**: `training-manual.md` → Evidence Submission SOP

```yaml
scenario: evidence_submission_simulation
role: Compliance Manager
steps:
  - prompt: "How do I start submitting evidence?"
    reply: "Begin by identifying the `Control_ID` you are supporting in `compliance-checklist.csv`."
  - prompt: "I’ve got the control — now what?"
    reply: "Gather your supporting materials: policy file, screenshot, log file, or scan result."
  - prompt: "How do I know what metadata I need?"
    reply: "Include `control_id`, `submitted_by`, `document_url`, and `notes`. These match the API schema from `api-specifications.json`."
  - prompt: "Where do I submit it?"
    reply: "You can use our internal ticketing system or POST the payload to the `/evidence` endpoint of our Compliance API."
  - prompt: "How is submission status tracked?"
    reply: "It’s logged in `submission-log.csv` and updated to `Pending Review` or `Complete` once validated."
```

---

## 🔄 Scenario: `access_revocation_simulation`

**Role**: IT Admin
**SOP**: Part of Offboarding + Security Practices

```yaml
scenario: access_revocation_simulation
role: IT Admin
steps:
  - prompt: "I received a termination notice — what’s my first step?"
    reply: "Verify the departure date and prepare to revoke credentials on the employee’s final working day."
  - prompt: "Which systems should I target?"
    reply: "Revoke access to email, VPN, SSO, admin consoles, SaaS apps, and internal servers. Use your standard system access checklist."
  - prompt: "How do I document this?"
    reply: "Log revocation timestamps in `submission-log.csv` or generate screenshots as evidence."
  - prompt: "Is that enough for audit purposes?"
    reply: "Yes, as long as evidence shows access was removed promptly and matches the official offboarding checklist from `training-manual.md`."
```

---

## 🔄 Scenario: `incident_response_simulation`

**Role**: Security Engineer
**SOP**: Not yet documented (suggested future SOP)

```yaml
scenario: incident_response_simulation
role: Security Engineer
steps:
  - prompt: "An alert came in — what should I do first?"
    reply: "Start by confirming the alert source and severity. Is this a real incident or a false positive?"
  - prompt: "It’s real — credentials exposed in a GitHub repo."
    reply: "Immediately revoke any exposed credentials and rotate associated secrets. Open an incident ticket."
  - prompt: "How should I document this?"
    reply: "Create an incident log entry including `timestamp`, `scope`, `actions taken`, and link it to the alert source."
  - prompt: "Do I need to notify compliance or leadership?"
    reply: "Yes, follow the escalation tree. For any breach of regulated data (e.g., PCI), notify within the required time window."
  - prompt: "How do I close the loop?"
    reply: "Perform root cause analysis and include post-incident notes in the incident tracker."
```

---

