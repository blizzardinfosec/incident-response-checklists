# ☸️ Kubernetes Incident Response Checklist

## 🧠 Triage
- [ ] Confirm detection source (Falco, EDR, logs, alerts)
- [ ] Identify suspicious namespace, pod, or node
- [ ] Determine workload owner (CI/CD? DevOps? Third-party?)

## 🔒 Containment
- [ ] `kubectl cordon` affected node
- [ ] `kubectl drain` node (if needed)
- [ ] `kubectl delete pod <name>` suspicious pod(s)
- [ ] Revoke ServiceAccount secrets in namespace
- [ ] Review network policies & egress rules

## 📦 Evidence Collection
- [ ] `kubectl logs` (stdout/stderr of affected pod)
- [ ] `kubectl get pod -o yaml` (save config & metadata)
- [ ] Dump node or container memory (if possible)
- [ ] Save image hashes and deployment manifests

## 🧹 Remediation
- [ ] Force redeploy from clean source
- [ ] Rotate secrets, tokens, and SA bindings
- [ ] Patch vulnerable container images or K8s CVEs
