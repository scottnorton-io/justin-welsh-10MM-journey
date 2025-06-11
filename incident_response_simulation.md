# 🚨 Incident Response Simulation

**Filename**: `incident_response_simulation.md`  
**Version**: 1.0  
**Last Updated**: 2025-06-11  
**Persona**: Security Engineer  
**Category**: SOP Simulation  
**Status**: Active (SOP pending)  

---

## 🎯 Purpose

This Training Mode scenario simulates a real-world incident response situation to help security engineers:

- Practice escalation and containment steps  
- Understand evidence documentation requirements  
- Rehearse compliance-aware decision making  

It is aligned with emerging controls such as `CC-9.4` and `CC-10.2` (audit logs, incident readiness) and supports integration with an internal incident response SOP when published.

---

## 🔄 Simulation Script

```yaml
scenario: incident_response_simulation
role: Security Engineer
steps:
  - prompt: "An alert just came in — what should I do first?"
    reply: "Verify the source and severity of the alert. Determine if it’s a false positive or an actual incident."

  - prompt: "It’s real — looks like credentials were exposed in a public GitHub repo."
    reply: "Immediately revoke the exposed credentials and rotate any impacted secrets. Document initial containment actions."

  - prompt: "Do I need to isolate any systems?"
    reply: "If any active systems were compromised, isolate them from the network to prevent further impact. Coordinate with IT and Compliance."

  - prompt: "How do I document this?"
    reply: "Log the incident in the incident tracker including: `timestamp`, `systems affected`, `remediation steps`, and any screenshots or logs."

  - prompt: "Should I notify leadership or compliance?"
    reply: "Yes — notify your Compliance Manager immediately if there’s potential for regulatory exposure (e.g., PCI, HIPAA). Include a brief impact summary."

  - prompt: "How do I close the incident?"
    reply: "Conduct a root cause analysis. Document lessons learned and file all artifacts in the `evidence_submission` system for later audits."

  - prompt: "Where should all this go?"
    reply: "Reference the `submission-log.csv` and tag entries under `Control_ID = CC-9.4` or equivalent. You can also initiate a policy update if response protocols were unclear."
