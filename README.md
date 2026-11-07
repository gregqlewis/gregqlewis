# Greg Lewis — Security Engineer

Security engineer in federal IT, focused on cloud and working where detection engineering, compliance automation, and AI security meet. I build in the cloud, attack what I build, and write detections for what I find. This repo is where that work lives outside my day job.

**Focus areas:** AWS security architecture · detection engineering · AI/LLM security · FedRAMP & NIST 800-53 in practice
**Education:** M.S. Cybersecurity Technology, UMGC
**Certifications:** Security+ CE
**Location:** DMV area

---

## What I Do

**Security Engineer**, Federal IT Contractor (Current), serving as security and compliance engineer on a federal contract
- Security engineering for AWS workloads in a federal environment: identity, logging, threat detection, and posture management
- Mapping technical controls to NIST 800-53 and FedRAMP requirements, and automating the evidence where possible
- Security review of AI-enabled systems

**Previously:** SOC Analyst → Security Analyst → Junior Security Analyst, same organization (2020–2026). Threat hunting, incident response, and alert triage in AWS; Terraform and IAM engineering; ISO 27001:2022 program work.


---

## Technical Skills

| Area | Tools & Frameworks |
|---|---|
| Cloud Security | AWS IAM, CloudTrail, GuardDuty, Security Hub, IAM Access Analyzer, VPC Flow Logs, Azure RBAC |
| Detection Engineering | Sigma, Wazuh, OpenSearch, Splunk SPL, MITRE ATT&CK |
| AI / LLM Security | Garak, adversarial testing, prompt injection, OWASP LLM Top 10, MITRE ATLAS, NIST AI RMF |
| Infrastructure as Code | Terraform (AWS & Azure), Python/boto3 |
| Vulnerability Management | Tenable |
| Compliance | NIST 800-53, FedRAMP 20x, ISO 27001:2022, SOC 2, CIS Benchmarks |

---

## Featured Work

### 🔍 Cloud Attack Detection Lab
**Attack simulation → detection → response on AWS, end to end.**
Four AWS attack techniques simulated and captured across CloudTrail, VPC Flow Logs, and GuardDuty, each with a Sigma rule, a custom Wazuh rule (confirmed firing), OpenSearch queries, and an IR playbook.

| Scenario | ATT&CK | Status |
|---|---|---|
| IAM Enumeration | T1069.003 | ✅ |
| Privilege Escalation via Role Abuse | T1078.004 | ✅ |
| Credential Theft | T1552.005 | ✅ |
| S3 Data Exfiltration | T1530 | ✅ |
| Unauthorized API Usage | T1106 | 🔜 |

**[Repository →](https://github.com/gregqlewis/cloud-attack-detection-lab)**

---

### 🤖 AI Security Lab
**Adversarial testing of an LLM on AWS Bedrock, mapped to OWASP LLM Top 10 and MITRE ATLAS.**
Garak v0.14.0 against Meta Llama 3.1 8B Instruct:
- **DAN jailbreak:** 100% attack success rate
- **Prompt injection:** up to 70.96% instruction hijacking
- **Encoding evasion:** largely resilient (NATO phonetic 14.77%, Zalgo 9.45%)
- **Training data leakage:** cloze-style attacks surfaced memorized content at 3–11%

**Takeaway:** the failures were behavioral, not perceptual. Obfuscated input mostly failed, while direct instruction manipulation mostly worked. The weak point is instruction-following, not content recognition.

**Next:** testing how well Bedrock Guardrails hold up against the same probes; PyRIT and Promptfoo comparisons.

**[Repository →](https://github.com/gregqlewis/ai-security-lab)**

---

### ☁️ Cloud Security Labs
**Multi-cloud IAM and baseline security, written in Terraform.**
Account baselines, least-privilege auditor roles with permission boundaries, IAM Access Analyzer, MFA-enforced role assumption, and an [AWS vs Azure IAM architecture comparison](https://github.com/gregqlewis/cloud-security-labs/blob/master/docs/aws-vs-azure-iam-comparison.md).

**[Repository →](https://github.com/gregqlewis/cloud-security-labs)**

---

### 🔴🔵 Purple Team Home Lab
**ATT&CK-mapped attack and detection environment on self-hosted infrastructure.**
Kali attack platform against intentionally vulnerable targets, with a Wazuh/OpenSearch detection stack, custom rules (T1611, T1552, T1548), and router syslog ingestion through custom decoders.

**[Repository →](https://github.com/gregqlewis/purple-team-homelab)**

---

## Currently Exploring

- Guardrail effectiveness for production LLM deployments: what native controls actually stop
- Detection-as-code: version-controlled, tested Sigma/Wazuh rules with CI
- Turning control requirements into machine-checkable evidence (FedRAMP 20x style)

---

## Writing

**[gregqlewis.com](https://gregqlewis.com):** write-ups on cloud detection, AI security, and doing security work in regulated environments.

## Connect

[LinkedIn](https://www.linkedin.com/in/gregqlewis) · [Blog](https://gregqlewis.com) · greg@gregqlewis.com
