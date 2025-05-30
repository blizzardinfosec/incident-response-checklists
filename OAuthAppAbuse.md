# 🧾 Malicious OAuth App Abuse Response

**MITRE ATT&CK Techniques**:  
- Credential Access: `T1528` (Steal Application Access Token)  
- Persistence: `T1098.001` (Account Manipulation)

## 🚨 Detection Triggers
- [ ] New app authorized without user login (e.g., via phishing link)
- [ ] App consent with excessive permissions (e.g., `Mail.ReadWrite`, `Files.ReadWrite.All`)
- [ ] OAuth grant event from unknown IP/device

## 🔒 Containment
- [ ] Revoke app token/consent via:
  - O365 → Azure Portal or Microsoft Graph
  - Google → Admin Console → App access control
  - Okta → Remove OAuth grants
- [ ] Reset user’s password and force logout
- [ ] Review session tokens for re-use or hijack

## 🧪 Investigation
- [ ] Review `user.oauth2.grant` or equivalent events
- [ ] Check scope of access requested
- [ ] Identify data access via granted permissions
- [ ] Look for multiple users consenting to the same app

## 🛠️ Remediation
- [ ] Block app registration (if org-wide open)
- [ ] Enable admin consent workflow for all third-party apps
- [ ] Monitor for abnormal Graph API usage

## 📝 Documentation
- [ ] List of affected users and scopes granted
- [ ] Timeline of app behavior
- [ ] Permanent config changes made
