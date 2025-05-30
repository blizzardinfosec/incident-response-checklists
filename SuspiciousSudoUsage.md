# 🧬 Suspicious Sudo Usage Response (Linux)

**MITRE ATT&CK Techniques**:  
- Privilege Escalation: `T1548.003` (Sudo and Sudo Caching)

## 🚨 Detection Triggers
- [ ] `sudo` executed with `-S` flag (piped password)
- [ ] `sudo` activity without associated user shell activity
- [ ] Commands like `sudo bash`, `sudo su`, or `sudo cp /bin/bash /tmp/shell && chmod +s`

## 🔒 Containment
- [ ] Identify and suspend account if unauthorized use
- [ ] Isolate host if compromise is suspected
- [ ] Audit `sudoers` and `/etc/sudoers.d/` for abuse

## 🧪 Investigation
- [ ] Review command history and `.bash_history`
- [ ] Analyze `/var/log/auth.log`, `auditd`, or EDR logs
- [ ] Check for privilege escalation tools or binaries

## 🛠️ Remediation
- [ ] Rotate root and privileged credentials
- [ ] Disable password reuse via `sudo -S`
- [ ] Restrict `sudo` usage to named commands where possible

## 📝 Documentation
- [ ] User timeline
- [ ] Logs of all elevated activity
- [ ] Defensive changes made (NIST 800-53/800-171 mapping optional)
