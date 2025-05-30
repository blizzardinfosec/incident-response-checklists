# 🛡️ Okta Account Compromise Response

**MITRE ATT&CK Techniques**:  
- Initial Access: `T1078` (Valid Accounts)  
- Defense Evasion: `T1556` (Impair Authentication)

## 🚨 Detection Indicators
- [ ] Sign-in with unusual geo/IP/device
- [ ] Legacy or basic auth used
- [ ] Session hijack via stolen token
- [ ] 3rd-party OAuth grant abuse

## 🔒 Containment
- [ ] Force logout of all sessions
- [ ] Reset password and MFA
- [ ] Disable account if necessary
- [ ] Check app token grants

## 🧪 Investigation
- [ ] Review sign-in timeline (Okta logs)
- [ ] Compare MFA success/fail attempts
- [ ] Identify linked apps and integrations
- [ ] Query for activity involving risky apps

## 🛠️ Remediation
- [ ] Invalidate all tokens
- [ ] Remove/rotate admin API tokens
- [ ] Enable phishing-resistant MFA (FIDO2, Okta Verify Push)

## 📄 Documentation
- [ ] List of impacted users/apps
- [ ] Indicators of compromise
- [ ] Mitigations added (MFA enforcement, alerts)
