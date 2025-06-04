# 🖥️ EDR Host Compromise Checklist

## 🧠 Triage
- [ ] Review EDR alert details (detection name, rule, confidence)
- [ ] Validate user identity (internal/external actor?)
- [ ] Identify lateral movement or secondary infections

## 🔒 Containment
- [ ] Isolate host via EDR (CrowdStrike/SentinelOne/MDE)
- [ ] Cut off VPN access (disable AD/SSO account if needed)
- [ ] Notify internal incident response team

## 📦 Evidence Collection
- [ ] Pull memory, disk artifacts via EDR (raw logs, binaries)
- [ ] Run DFIR triage tool (e.g. Velociraptor, KAPE, or GRR)
- [ ] Snapshot host or disk image (if feasible)
- [ ] Collect browser history, scheduled tasks, and autoruns

## 🧹 Remediation
- [ ] Wipe and reimage host (if integrity is lost)
- [ ] Rotate compromised credentials
- [ ] Re-enable MFA or conditional access
