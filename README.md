# 📘 Incident Response Checklists

This repo contains operational, markdown-based IR playbooks and checklists built for fast-moving blue teams responding to real-world attacks across cloud, SaaS, endpoints, and Kubernetes environments.

---

## 🧠 Guiding Principles

- 📍 Mapped to [MITRE ATT&CK](https://attack.mitre.org/)
- 🛠️ Focused on **containment**, **evidence collection**, and **response speed**
- ⚡ Written for use **during the incident**, not just postmortem
- 👩‍💻 Designed for SOC analysts, detection engineers, and incident responders

---

## ✅ Included Playbooks

| Name                            | Focus Area                         |
|---------------------------------|------------------------------------|
| `business_email_compromise.md`  | Microsoft 365 / Email / MFA abuse  |
| `ransomware_outbreak.md`        | Endpoint & file-level containment  |
| `aws_cloudbreach.md`            | AWS account & key compromise       |
| `kubernetes_incident.md`        | Pod/cluster compromise in K8s      |
| `edr_host_compromise.md`        | CrowdStrike/S1/MDE host triage     |
| `o365_account_takeover.md`      | SaaS mailbox & user compromise     |
| `okta_breach_response.md`       | (Coming soon) IdP compromise       |

---

## 🧰 Usage

Each checklist is written in Markdown and optimized for live use in:
- Secure Notebooks (Jupyter, Obsidian, etc.)
- SOAR runbooks
- Tabletop exercises
- Command-line responders or IR dashboards

---

## 🚧 Roadmap

- [ ] Add Google Workspace incident checklist  
- [ ] Build PDF/Obsidian export pipeline  
- [ ] MITRE tags auto-index per checklist  
- [ ] Create public test suite for tabletop validation

---

📎 These are not compliance policies — they’re what you reach for **when systems are burning**.
