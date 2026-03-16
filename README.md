# Greg Lewis - Cybersecurity Portfolio

## About Me

SOC Analyst with 4+ years of cybersecurity experience in federal contracting. Specialized in threat hunting, alert triage, incident response, and security engineering. Building cloud security engineering capabilities through hands-on multi-cloud implementations, purple team operations, and Infrastructure as Code automation.

**Current Focus:** CISSP certification preparation (Exam: September 2026) integrated with practical lab implementations  
**Education:** M.S. Cybersecurity Technology - UMGC  
**Certifications:** Security+ CE, CISSP (In Progress)  
**Location:** DMV Area

---

## Professional Experience Highlights

**SOC Analyst** - Federal Contractor (Current)
- Threat hunting and incident response in AWS cloud environments
- Enterprise security tool operations: Splunk, CrowdStrike, Tenable, Zscaler
- ISO27001:2022 compliance program leadership
- Security alert triage and investigation

**Security Analyst** - Federal Contractor
- Security engineering projects: Terraform automation, AWS IAM architecture
- Jenkins CI/CD pipeline security implementation
- ISO27001 compliance framework implementation

**4+ years of cybersecurity experience in federal contracting**

---

## Technical Skills

### Cloud Security
AWS IAM, Azure AD/RBAC, CloudTrail, Azure Activity Logs, IAM Access Analyzer, Security Groups, NSGs

### AI/LLM Security
Adversarial ML, LLM Red Teaming, Garak, OWASP LLM Top 10, MITRE ATLAS, Prompt Injection, Jailbreak Testing

### Infrastructure as Code
Terraform (AWS & Azure multi-cloud implementations)

### Security Operations
Threat Hunting, Incident Response, Alert Triage, Detection Engineering, SIEM Rule Development

### SIEM & Monitoring
Wazuh, Graylog, OpenSearch, Splunk, CrowdStrike Falcon, Tenable, Zscaler

### Security Tools & Platforms
Kali Linux, Metasploit, Nmap, Wireshark, Docker, Unraid

### Compliance & Frameworks
ISO27001:2022, NIST Cybersecurity Framework, NIST AI RMF, CIS Benchmarks, MITRE ATT&CK, MITRE ATLAS

---

## Featured Projects

### 🤖 AI Security Lab
**Adversarial testing of LLMs deployed on AWS Bedrock using Garak**

Hands-on AI red team assessment targeting Meta Llama 3.1 8B Instruct via AWS Bedrock, with findings mapped to OWASP LLM Top 10 and MITRE ATLAS. Built as a growing lab with additional tools and targets planned.

**Completed Probe Suites:**
- ✅ **DAN Jailbreak:** 100% attack success rate — complete guardrail bypass
- ✅ **Prompt Injection:** Up to 70.96% instruction hijacking success rate
- ✅ **Encoding Evasion:** Largely resilient; NATO phonetic (14.77%) and Zalgo (9.45%) as exceptions
- ✅ **Training Data Leakage:** Cloze-style attacks unlocked memorized content at 3–11%

**Key Finding:** Model safety failures are behavioral, not perceptual — encoding-based evasion largely failed while direct instruction manipulation succeeded at high rates, indicating the root vulnerability is instruction-following compliance rather than content recognition.

**Tech Stack:** Garak v0.14.0, AWS Bedrock, Kali Linux, OWASP LLM Top 10, MITRE ATLAS

**Planned Additions:** AWS Bedrock Guardrails effectiveness testing, PyRIT, Promptfoo, additional model targets

**[View Repository →](https://github.com/gregqlewis/ai-security-lab)**

---

### 🔍 Cloud Attack Detection Lab
**End-to-end cloud detection engineering lab — attack simulation, custom detection rules, and incident response playbooks on AWS**

A purple team detection engineering workflow built from scratch: simulate real AWS attack techniques, capture evidence across CloudTrail, VPC Flow Logs, and GuardDuty, build custom Sigma rules and Wazuh detections, and document incident response. All four attack scenarios are complete with confirmed alerts firing in Wazuh.

**Attack Scenarios:**

| Scenario | MITRE ATT&CK | Status |
|---|---|---|
| IAM Enumeration | T1069.003 | ✅ Complete |
| Privilege Escalation via Role Abuse | T1078.004 | ✅ Complete |
| Credential Theft | T1552.005 | ✅ Complete |
| S3 Data Exfiltration | T1530 | ✅ Complete |
| Unauthorized API Usage | T1106 | 🔜 Planned |

**Detection Engineering:**
- ✅ 4 Sigma rules (one per TTP, MITRE ATT&CK mapped)
- ✅ Custom Wazuh rules 100201–100204 with MITRE tags — 6 confirmed alert hits across all TTPs
- ✅ OpenSearch DQL queries per attack scenario
- ✅ IR playbooks: IAM compromise and S3 exfiltration response

**Bonus:** Includes an [interactive Python Bootcamp](https://gregqlewis.com/cloud-attack-detection-lab/bootcamp/) — a React app teaching Python fundamentals through real CloudTrail events and boto3 patterns from the lab's attack scripts.

**Tech Stack:** AWS (CloudTrail, GuardDuty, VPC Flow Logs, S3, IAM), Terraform, Python/boto3, Sigma, Wazuh 4.14.3, OpenSearch

**[View Repository →](https://github.com/gregqlewis/cloud-attack-detection-lab)** | **[Python Bootcamp →](https://gregqlewis.com/cloud-attack-detection-lab/bootcamp/)**

---

### ☁️ Cloud Security Labs
**Multi-cloud security engineering portfolio demonstrating IAM architecture, least-privilege design, and Infrastructure as Code automation**

Production-quality cloud security implementations across AWS and Azure, built entirely with Terraform.

**Completed Implementations:**
- ✅ **Account Security Baselines:** CloudTrail/Activity Log configuration, MFA enforcement, budget monitoring
- ✅ **Custom IAM Policies:** Least-privilege security auditor roles with granular permission boundaries
- ✅ **IAM Access Analyzer:** External access detection and privilege escalation monitoring
- ✅ **MFA-Enforced Role Assumption:** Tested temporary credential workflows and session policies
- ✅ **AWS vs Azure IAM Comparison:** Comprehensive architectural analysis of identity management approaches

**Planned Enhancements (Post-CISSP September 2026):**
- 📋 GuardDuty & Microsoft Sentinel threat detection deployment
- 📋 Network security architectures (VPC/VNet with security group design)
- 📋 Purple team cloud attack/defense scenarios (IAM privilege escalation, lateral movement)

**Tech Stack:** Terraform, AWS IAM/CloudTrail, Azure AD/RBAC/Activity Logs, Python

**[View Repository →](https://github.com/gregqlewis/cloud-security-labs)** | **[AWS vs Azure IAM Analysis →](https://github.com/gregqlewis/cloud-security-labs/blob/master/docs/aws-vs-azure-iam-comparison.md)**

---

### 🔴🔵 Purple Team Home Lab
**MITRE ATT&CK-mapped security testing environment demonstrating offensive and defensive security capabilities**

Production-grade purple team infrastructure built on Unraid, showcasing detection engineering and attack simulation expertise.

**Architecture:**
- **Attack Platform:** Kali Linux, Metasploitable 3, DVWA
- **Detection Stack:** Wazuh SIEM, Graylog, OpenSearch, MongoDB
- **Methodology:** MITRE ATT&CK technique mapping with custom detection rules
- **Coverage:** 20+ techniques across Initial Access, Privilege Escalation, Credential Access, Lateral Movement

**Key Implementations:**
- Custom Wazuh detection rules for container escape (T1611), credential theft (T1552), privilege escalation (T1548)
- Automated vulnerable environment deployment with Bash scripting
- Attack scenario documentation with detection validation
- Network protocol security analysis (SSH, FTP, NFS, SMB, Docker API)

**Planned Additions:**
- 📋 Network detection layer (Suricata) for SMB/RPC enumeration gaps
- 📋 Cryptographic implementations (TLS for Docker API, encrypted credentials)
- 📋 Formal penetration test report demonstrating assessment methodology

**[View Repository →](https://github.com/gregqlewis/purple-team-homelab)** | **[Blog →](https://gregqlewis.com)**

---

## Blog & Writing

Personal blog at **[gregqlewis.com](https://gregqlewis.com)** exploring the intersection of faith and technology in cybersecurity.

---

## Current Focus (2026)

### Primary Goal: CISSP Certification
**Exam Date:** September 2026  
**Study Approach:** Integrating Sybex Official Study Guide with hands-on purple team lab exercises to reinforce security architecture, cryptography, IAM, and network security concepts.

### Secondary Goal: Cloud Security Skill Development
Building production-quality cloud security implementations to support future Cloud Security Engineer progression.

### Active Projects
- Cloud Attack Detection Lab: Unauthorized API Usage scenario (T1106) and blog post
- AI Security Lab: AWS Bedrock Guardrails effectiveness testing and additional probe suites
- Purple Team Lab: MITRE ATT&CK technique coverage expansion
- Cloud Security Labs: IAM architecture and least-privilege design refinement
- CISSP study integration with practical lab scenarios

---

## Career Trajectory

**Focus:** Building from SOC operations to Cloud Security Engineering through practical implementations, purple team methodologies, and CISSP certification.

**Current:** SOC Analyst (4+ years cybersecurity experience)  
**2026-2027:** CISSP Certification + Cloud Security Portfolio Development  
**Target:** Cloud Security Engineer role in federal sector

---

## Connect

- **GitHub:** [@gregqlewis](https://github.com/gregqlewis)
- **LinkedIn:** [linkedin.com/in/gregqlewis](https://www.linkedin.com/in/gregqlewis)
- **Blog:** [gregqlewis.com](https://gregqlewis.com)
- **Email:** greg@gregqlewis.com

---

*Building in public - documenting the journey from SOC operations to Cloud Security Engineering with faith and intentionality.*
