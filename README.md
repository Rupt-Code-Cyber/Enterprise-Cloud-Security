# Enterprise Cloud Security Posture Assessment & Hardening Lab

![AWS](https://img.shields.io/badge/AWS-Cloud-orange)
![Cloud Security](https://img.shields.io/badge/Cloud-Security-blue)
![Security](https://img.shields.io/badge/Security-Assessment-red)
![MITRE ATT&CK](https://img.shields.io/badge/MITRE-ATT%26CK-green)
![CVSS v3.1](https://img.shields.io/badge/CVSS-v3.1-yellow)
![License](https://img.shields.io/badge/License-MIT-lightgrey)

---

# Executive Summary

This project demonstrates a complete enterprise-style cloud security assessment of an Amazon Web Services (AWS) environment.

The assessment was performed against an intentionally configured cloud laboratory to identify security weaknesses, evaluate risk, implement remediation, and validate improvements.

The project follows security engineering and consulting practices commonly used during professional cloud security assessments.

---

# Project Objectives

- Assess AWS cloud security posture
- Identify security misconfigurations
- Evaluate business risk
- Map findings to MITRE ATT&CK
- Prioritize findings using CVSS v3.1
- Implement security hardening
- Validate remediation
- Produce enterprise-grade documentation

---

# Lab Architecture

Architecture documentation:

```
architecture/
```

Network diagram:

```
architecture/network-diagram.png
```

---

# Assessment Scope

The following AWS services were included in the assessment.

| Area | Services |
|------|----------|
| Identity | IAM |
| Networking | VPC, Security Groups |
| Compute | EC2 |
| Storage | Amazon S3 |
| Monitoring | CloudTrail |
| Threat Detection | GuardDuty |
| Security Management | Security Hub |
| Compliance | AWS Config |

---

# Assessment Methodology

The assessment followed a structured five-phase methodology.

```
Planning

↓

Discovery

↓

Assessment

↓

Remediation

↓

Validation
```

Detailed methodology:

```
documentation/security-assessment-methodology.md
```

---

# Security Findings

| Finding | Severity | Status |
|----------|----------|--------|
| Internet Exposed SSH | Critical | Remediated |
| Public S3 Bucket | High | Remediated |
| Excessive IAM Permissions | High | Remediated |
| Limited Monitoring | Medium | Improved |

---

# Risk Rating Summary

| Severity | Count |
|----------|------:|
| Critical | 1 |
| High | 2 |
| Medium | 1 |
| Low | 0 |

---

# CVSS Risk Scoring

The vulnerabilities were prioritized using CVSS v3.1.

| Finding | Score | Severity |
|----------|------:|----------|
| Internet Exposed SSH | 9.8 | Critical |
| Excessive IAM Permissions | 8.8 | High |
| Public S3 Bucket | 8.2 | High |
| Limited Monitoring | 4.4 | Medium |

Detailed report:

```
reports/cvss-risk-scoring.md
```

---

# MITRE ATT&CK Mapping

Mapped techniques include:

| Technique | Description |
|-----------|-------------|
| T1133 | External Remote Services |
| T1078 | Valid Accounts |
| T1530 | Data from Cloud Storage |
| T1562 | Impair Defenses |
| T1580 | Cloud Infrastructure Discovery |

Full mapping:

```
mitre/attack-mapping.md
```

---

# Security Improvements

The following improvements were implemented during the assessment.

## Identity

- Least Privilege IAM
- MFA recommendations
- Permission review

## Network

- Restricted SSH access
- Reduced attack surface
- Improved Security Groups

## Storage

- Block Public Access
- Encryption enabled
- Bucket policy review

## Monitoring

- CloudTrail enabled
- GuardDuty enabled
- AWS Config enabled
- Security Hub enabled

---

# Technologies Used

## Cloud

- Amazon Web Services

## Security

- AWS IAM
- Amazon VPC
- EC2
- Amazon S3
- CloudTrail
- GuardDuty
- AWS Config
- Security Hub

## Assessment

- ScoutSuite
- Prowler

## Documentation

- Markdown
- Draw.io
- Git
- GitHub

---

# Repository Structure

```
enterprise-cloud-security-posture-assessment/

├── architecture/
│   ├── architecture.md
│   ├── network-diagram.drawio
│   └── network-diagram.png
│
├── documentation/
│   ├── aws-security-controls.md
│   ├── cloud-environment-setup.md
│   ├── cloud-hardening-guide.md
│   ├── security-assessment-methodology.md
│   └── vulnerability-management.md
│
├── incidents/
│   └── security-assessment-results.md
│
├── mitre/
│   └── attack-mapping.md
│
├── reports/
│   ├── executive-summary.md
│   └── cvss-risk-scoring.md
│
├── screenshots/
│
├── LICENSE
│
└── README.md
```

---

# Screenshots

Add screenshots to the `screenshots/` directory, including:

- AWS Console overview
- ScoutSuite findings
- Prowler results
- IAM configuration
- Security Group changes
- S3 permissions
- CloudTrail
- GuardDuty
- Security Hub
- AWS Config
- Architecture diagram
- Documentation previews

---

# Skills Demonstrated

- AWS Cloud Security
- Cloud Security Assessment
- Security Posture Review
- Identity & Access Management
- Network Security
- Threat Detection
- Vulnerability Management
- CVSS Risk Assessment
- MITRE ATT&CK Mapping
- Security Hardening
- Technical Documentation
- Risk Communication
- Git & GitHub

---

# Future Improvements

Future enhancements may include:

- AWS Organizations
- AWS Control Tower
- AWS IAM Identity Center
- AWS Network Firewall
- Amazon Inspector
- Amazon Detective
- Security Information and Event Management (SIEM) integration
- Security Orchestration, Automation, and Response (SOAR)
- Infrastructure as Code (Terraform)
- Continuous compliance pipelines

---

# License

This project is licensed under the MIT License.

See the `LICENSE` file for details.

---

# Author

**Your Name**

Cloud Security Engineer

GitHub:

```
https://github.com/YOUR_USERNAME
```

LinkedIn:

```
https://linkedin.com/in/YOUR_PROFILE
```