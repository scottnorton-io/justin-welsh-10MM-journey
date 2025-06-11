# 💻 Code Snippets Library

**Filename**: `code-snippets-library.md`
**Version**: 1.0
**Last Updated**: 2025-06-11

---

## 🎯 Purpose

This addendum contains a curated set of code snippets and script patterns the GPT assistant can:

* Reference when creating technical validation instructions
* Embed in procedures, SOPs, or policy guidance
* Use as starter templates for automation, scripting, or compliance evidence gathering

Each snippet is labeled by language, usage category, and applicable persona (see `user-personas.md`), and includes inline comments for clarity.

---

## 🧪 Usage Guidelines

* Output snippets when prompted to validate controls, automate tasks, or transform configs
* Cite snippet name when reused from this file
* Adapt snippets with environment-specific paths or settings when user provides context

---

## 🛡️ Snippet: Verify TLS Configuration (Bash)

**Language**: Bash
**Persona**: Engineer
**Use Case**: Verify supported TLS versions and cipher suites for a given endpoint

```bash
#!/bin/bash
DOMAIN="example.com"
PORT=443

echo "Checking supported TLS protocols for $DOMAIN:$PORT"
for version in ssl2 ssl3 tls1 tls1_1 tls1_2 tls1_3; do
  echo -n "$version: "
  echo | openssl s_client -connect $DOMAIN:$PORT -$version 2>/dev/null | grep "Protocol" || echo "Not supported"
done
```

---

## 🔐 Snippet: Check File Encryption with AES-256 (Linux)

**Language**: Bash
**Persona**: Engineer
**Use Case**: Confirm that a file is encrypted with AES-256

```bash
#!/bin/bash
FILE="sensitive-data.enc"

echo "Checking encryption method for $FILE..."
file $FILE | grep -q "AES-256" && echo "AES-256 confirmed" || echo "Encryption method unclear"
```

> 💡 Output can be redirected to compliance logs.

---

## 🗃️ Snippet: JSON Validation Script (Python)

**Language**: Python
**Persona**: Engineer
**Use Case**: Validate a JSON config file against required fields

```python
import json

required_fields = ["control_id", "submitted_by", "document_url"]

with open("evidence_payload.json") as f:
    data = json.load(f)

missing = [field for field in required_fields if field not in data]
if missing:
    print(f"Missing fields: {', '.join(missing)}")
else:
    print("All required fields present.")
```

---

## 📄 Snippet: Markdown Table Generator (Python)

**Language**: Python
**Persona**: Policy Owner
**Use Case**: Convert a CSV into a formatted Markdown table

```python
import csv

with open('gap-analysis.csv') as csvfile:
    reader = csv.reader(csvfile)
    rows = list(reader)

headers = rows[0]
print("| " + " | ".join(headers) + " |")
print("|" + "|".join(["---"] * len(headers)) + "|")

for row in rows[1:]:
    print("| " + " | ".join(row) + " |")
```

---

## 🧾 Snippet: SOP Template (Markdown)

**Language**: Markdown
**Persona**: Policy Owner / Compliance Manager
**Use Case**: Standard structure for new operating procedures

```md
# SOP Title

**Version**: 1.0  
**Effective Date**: YYYY-MM-DD  
**Review Date**: YYYY-MM-DD  
**Owner**: [Department or Person]

---

## Purpose
Brief description of why this SOP exists.

## Scope
What processes or roles this SOP applies to.

## Responsibilities
List of roles and their duties.

## Procedure
1. Step one...
2. Step two...
3. Final step...

## References
- `related-policy.md`
- External resource link

## Change Log
| Version | Date       | Changes         | Author         |
|---------|------------|------------------|----------------|
| 1.0     | YYYY-MM-DD | Initial version | Your Name      |
```

---

## 📤 Snippet: Evidence Submission (cURL API)

**Language**: Shell / cURL
**Persona**: Engineer / Auditor
**Use Case**: Programmatically submit evidence to a compliance API

```bash
curl -X POST https://api.example.com/v1/evidence \
  -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
  -H "Content-Type: application/json" \
  -d '{
    "control_id": "CC-3.1",
    "submitted_by": "alice@example.com",
    "document_url": "https://docs.example.com/evidence/ev-12345.pdf",
    "notes": "TLS scan screenshot attached"
}'
```

---

## 📎 Notes

* All scripts are templates. Adjust paths, credentials, and IDs as required.
* Each snippet should be saved with an identifying label in the `outputs-history.csv` if reused.
* Additional snippets may be added to support platform-specific tasks (e.g., AWS CLI, PowerShell).

---
