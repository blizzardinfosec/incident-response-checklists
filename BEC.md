# 📥 BEC Incident Response Checklist

**MITRE ATT&CK Techniques**:  
- Initial Access: `T1078` (Valid Accounts)  
- Command & Control: `T1102` (Web Service)

## 🔍 Initial Detection
- [ ] Alert from abnormal login behavior (Okta, Azure AD)
- [ ] Email forwarding rule created
- [ ] Login from unexpected geo or device
- [ ] Executive impersonation or invoice fraud attempt

## 🔒 Containment
- [ ] Reset password + MFA for affected account(s)
- [ ] Terminate active sessions (Okta, M365, etc.)
- [ ] Search for forwarding rules, mailbox delegations
- [ ] Disable account if needed

## 🧪 Investigation
- [ ] Review sign-in logs (IP, geo, user agent)
- [ ] Search inbox for keywords: “wire”, “invoice”, “gift card”
- [ ] Check for 3rd-party OAuth app grants (M365, Google)
- [ ] Investigate inbox rules, sharing settings

## 🧼 Remediation
- [ ] Revoke malicious sessions or OAuth grants
- [ ] Notify impacted contacts if impersonation occurred
- [ ] Tune detection rules based on IOCs
- [ ] Train user if compromise was due to phishing

## 📄 Documentation
- [ ] Timeline of attacker activity
- [ ] IOC list (IPs, apps, messages)
- [ ] Lessons learned and gaps found
