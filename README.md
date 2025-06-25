# 🧾 Code Audit Notes – AppSec Source Review Practice

This repository documents my manual code review notes as I analyze vulnerable applications, insecure code samples, and real-world patterns.

---

## 🔍 Focus Areas

- Authentication & Session Management flaws
- Broken Access Control (IDOR, role bypass)
- Input validation issues (XSS, injection)
- Insecure deserialization and logic flaws
- Token and JWT mishandling

---

## 📁 Folder Structure

- `insecure-auth/` – Weak login logic, token storage, password flaws
- `broken-access-control/` – Role logic bypasses, IDORs, privilege escalation
- `input-validation/` – Insecure inputs, unsanitized data, XSS points
- `payloads/` – Wordlists and snippets used during auditing

---

## 🧠 Skills Demonstrated

- Reading insecure code across languages (Python, JS, PHP)
- Identifying vulnerabilities without scanning tools
- Documenting exploit chains and remediations
- Applying OWASP Top 10 knowledge in source code form
