# ☁️ AWS Account Takeover Response

**MITRE ATT&CK Techniques**:  
- Initial Access: `T1078` (Valid Accounts)  
- Persistence: `T1078.004` (Cloud Accounts)

## 🚨 Detection Triggers
- [ ] `ConsoleLogin` from new geo or user agent
- [ ] Usage of root account
- [ ] High-risk `AssumeRole` usage
- [ ] Rapid IAM policy/role changes

## 🔒 Containment
- [ ] Disable IAM access keys
- [ ] Revoke sessions via AWS CLI
- [ ] Remove suspicious policies or roles
- [ ] Enable MFA on all affected accounts

## 🧪 Investigation
- [ ] Pull CloudTrail logs for:
  - `ConsoleLogin`, `AssumeRole`, `CreateUser`, `AttachPolicy`
- [ ] Check GuardDuty for indicators
- [ ] Verify CloudWatch alert coverage

## 🛠️ Remediation
- [ ] Rotate all credentials (IAM + 3rd-party)
- [ ] Reset audit trail config (CloudTrail, S3 buckets)
- [ ] Review VPC and SG changes

## 📝 Documentation
- [ ] Timeline of activity
- [ ] User/account mappings
- [ ] Permanent improvements (CSPM config, alert tuning)
