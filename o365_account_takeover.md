# 📧 Office 365 Account Takeover Checklist

## 🧠 Triage
- [ ] Alert source: abnormal login, phishing, MFA bypass?
- [ ] Validate login time, IP, user-agent
- [ ] Identify compromised mailbox activity (search/download/fwd)

## 🔒 Containment
- [ ] Disable user sign-in
- [ ] Revoke active sessions and refresh tokens
- [ ] Remove malicious inbox rules and external forwards

## 📦 Evidence Collection
- [ ] Export audit logs (`Search-UnifiedAuditLog`)
- [ ] Review Azure AD sign-in logs
- [ ] Download mailbox activity logs (via eDiscovery)

## 🧹 Remediation
- [ ] Reset password + enforce strong auth (MFA, conditional access)
- [ ] Notify user and force password reset across other systems
- [ ] Report incident in compliance platform (HIPAA, GDPR, etc.)
