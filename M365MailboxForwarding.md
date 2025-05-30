# 📤 Suspicious M365 Mailbox Forwarding Rules

**MITRE ATT&CK Techniques**:  
- Collection: `T1114.003` (Email Collection via Auto-Forward Rules)  
- Exfiltration: `T1020` (Automated Exfil via Forwarding)

## 🚨 Detection Triggers
- [ ] New inbox rule to forward all mail externally
- [ ] `Set-InboxRule` or `New-InboxRule` activity via PowerShell
- [ ] Mail flow anomalies (burst SMTP send, unexpected relay)

## 🔒 Containment
- [ ] Remove inbox forwarding rules
- [ ] Disable suspicious account or change credentials
- [ ] Audit connected devices (via Sign-in logs)

## 🧪 Investigation
- [ ] PowerShell logs → `Set-InboxRule` or `New-InboxRule`
- [ ] Unified Audit Log → `Add-MailboxPermission`, `SendOnBehalf`, `SendAs`
- [ ] Analyze contents of forwarded messages (DLP)

## 🛠️ Remediation
- [ ] Block auto-forward to external domains
- [ ] Alert on rule creation with `forward`, `bcc`, or `delete`
- [ ] Require conditional access for Exchange Online access

## 📝 Documentation
- [ ] Rule type, timestamps, affected inbox
- [ ] Forwarding target (domain/IP)
- [ ] Compromise timeline and remediation summary
