# CloudGuard

> Personal cloud‑security project on AWS ✨  
> _“Build it, break it, secure it.”_

## 1. What is CloudGuard?

CloudGuard is my end‑to‑end experiment in designing, deploying, and securing a mini AWS environment.  
The goal is to understand **networking, IAM, encryption, monitoring, and incident response** by building each piece.

> **Status:** early scaffolding – expect frequent rewrites.

## 2. High‑Level Roadmap

| Phase                          | Purpose                                  | Date Completed |
| ------------------------------ | ---------------------------------------- | -------------- |
| **0 — Foundations**            | Billing alarms, MFA, repo bootstrap      | 2025-06-25     |
| **1 — Networking Core**        | VPC, subnets, IGW/NAT, security groups   | TBD            |
| **2 — Compute Layer**          | EC2 (public & private) + SSM access      | TBD            |
| **3 — Secure Storage**         | Encrypted EBS + snapshots                | TBD            |
| **4 — Vulnerable App**         | Dockerised OWASP Juice Shop for testing  | TBD            |
| **5 — Infrastructure as Code** | Terraform modules & state mgmt           | TBD            |
| **6 — Security Services**      | WAF, GuardDuty, CloudTrail, Security Hub | TBD            |
| **7 — Hardening & Cleanup**    | Patching, key rotation, cost controls    | TBD            |

## 3. Getting Started

1. **Clone** the repo
   ```bash
   git clone https://github.com/<your‑user>/cloudguard.git
   ```
2. **Configure AWS credentials** (least‑privilege IAM user).
3. **Terraform init / apply** inside `/infra` when that folder appears.
4. **Track costs** – NAT Gateways aren’t free!

## 4. Milestone Checklist

- [x] Foundations complete (billing alarm fires at \$5.00 and again at \$7.75)
- [ ] Public EC2 reachable via SSH
- [ ] Private EC2 reachable only via SSM
- [ ] Juice Shop browsable through Nginx proxy
- [ ] Terraform 100 % parity with console resources
- [ ] GuardDuty shows demo findings
- [ ] Automated EBS snapshots in place

## 5. Progress Log

| Date (YYYY‑MM‑DD) | Commit              | Notes                 |
| ----------------- | ------------------- | --------------------- |
| 2025-06-25        | `init`              | Repository scaffolded |
| _TBD_             | `feat/network-core` | VPC + subnets + SGs   |


## 6. Progress Notes
**2025-06-25**
- Initial GItHub repo established
- AWS Budget created (max \$10.00, spending alerts at \$5.00 and \$7.75)
- AWS MFA enabled
- Project-Specific IAM User Established

## 7. Contributing / Licensing

Right now, this is a **solo learning project**. Feel free to open issues or PRs if you spot something unsafe or unclear.

All original content © 2025 Sam Holtzman. Code samples will be MIT‑licensed once they exist.

---

_This README is intentionally minimal and will evolve alongside the project._
