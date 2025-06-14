# 🔐 MFA Fatigue Attack

**Scenario:** Repeated MFA prompts sent to trick a user into approving access (common in Okta, Duo, Microsoft 365).

## 🧭 Goals
- Determine source of login attempt
- Identify affected accounts/devices
- Block access and reset credentials
- Investigate potential lateral movement

## ✅ Checklist
- [ ] Confirm MFA provider logs indicate push spam
- [ ] Identify IP address and geolocation of login attempt
- [ ] Review access logs for successful/failed logins
- [ ] Force password reset and revoke sessions
- [ ] Disable MFA method or switch to number matching/device auth
- [ ] Search for related activity in Okta, M365, Duo, etc.
- [ ] Run queries for unusual IPs, devices, and actions
- [ ] Review device health and endpoint alerts
- [ ] Communicate with user (voice preferred) to confirm behavior
