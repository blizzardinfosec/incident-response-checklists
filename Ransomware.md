# 🔐 Ransomware Incident Response Checklist

**MITRE ATT&CK Techniques**:  
- Execution: `T1059` (Command & Scripting Interpreter)  
- Impact: `T1486` (Data Encrypted for Impact)

## 🚨 Initial Indicators
- [ ] Endpoint alerts (CrowdStrike, Defender, etc.)
- [ ] File extensions renamed or encrypted
- [ ] User-reported issues accessing files

## 🔒 Containment
- [ ] Isolate affected endpoints
- [ ] Disable network shares temporarily
- [ ] Identify initial access vector (phishing, RDP, etc.)

## 🧪 Investigation
- [ ] Triage patient-zero machine
- [ ] Pull logs from EDR, SIEM, and sysmon
- [ ] Collect memory and disk images if needed
- [ ] Map lateral movement path
- [ ] Extract ransomware binary and calculate hash

## 📦 Recovery
- [ ] Restore from backups (offline if possible)
- [ ] Verify backup integrity before deploying
- [ ] Rebuild or reimage infected systems
- [ ] Rotate credentials (especially admin/service)

## 📄 Post-Incident
- [ ] Document scope and impact
- [ ] List of encrypted systems + timelines
- [ ] Lessons learned & detection coverage gaps
- [ ] Executive report or summary for legal/insurance
