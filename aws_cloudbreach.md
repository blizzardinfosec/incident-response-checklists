# ☁️ AWS Cloud Breach Checklist

## 🧠 Triage
- [ ] Confirm GuardDuty/CloudTrail findings
- [ ] Identify compromised user/role/session
- [ ] Check for IAM misconfigurations or role assumptions

## 🔒 Containment
- [ ] Disable IAM user/rotate credentials
- [ ] Revoke API tokens and kill sessions
- [ ] Isolate EC2 instance (remove from ELB, disable egress)

## 📦 Evidence Collection
- [ ] Save CloudTrail logs (event history)
- [ ] Export EC2 metadata, AMIs, and volume snapshots
- [ ] Pull logs from S3, VPC Flow Logs, GuardDuty, Config

## 🧹 Remediation
- [ ] Lock down IAM policies
- [ ] Rotate long-lived keys
- [ ] Apply service control policies (SCPs) to prevent recurrence
