# CVSS Security Scoring Report

## Enterprise Cloud Security Posture Assessment & Hardening Lab


---

# 1. Report Overview


This document provides vulnerability severity assessment using the Common Vulnerability Scoring System (CVSS) version 3.1 methodology.


CVSS scoring was used to evaluate:


- Attack complexity
- Required privileges
- User interaction requirements
- Confidentiality impact
- Integrity impact
- Availability impact


---

# 2. CVSS Methodology


CVSS v3.1 evaluates vulnerabilities using three metric groups:


## Base Metrics


Measures the fundamental characteristics of a vulnerability.


Includes:


- Attack Vector
- Attack Complexity
- Privileges Required
- User Interaction
- Scope
- Confidentiality
- Integrity
- Availability


---

## Severity Ratings


| Score | Severity |
|-|-|
| 0.0 | None |
| 0.1 - 3.9 | Low |
| 4.0 - 6.9 | Medium |
| 7.0 - 8.9 | High |
| 9.0 - 10.0 | Critical |


---

# 3. Vulnerability Assessment


# Finding 001 — Public S3 Bucket Exposure


## Description


A cloud storage resource was configured with public access permissions, creating potential unauthorized data exposure.


---

## CVSS Vector


```
CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:H/I:N/A:N
```


---

## Score


```
7.5
```


Severity:


```
High
```


---

## Metric Analysis


| Metric | Value | Reason |
|-|-|-|
| Attack Vector | Network | Accessible remotely |
| Attack Complexity | Low | Simple exploitation |
| Privileges Required | None | No authentication required |
| User Interaction | None | No user action needed |
| Confidentiality | High | Data exposure possible |
| Integrity | None | No modification capability |
| Availability | None | No service impact |


---

## Risk Explanation


Public cloud storage exposure can result in unauthorized disclosure of sensitive organizational information.


---

# Finding 002 — Internet Exposed SSH Access


## Description


The EC2 security group allowed SSH access from any internet source.


---

## CVSS Vector


```
CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:H/I:H/A:H
```


---

## Score


```
9.8
```


Severity:


```
Critical
```


---

## Metric Analysis


| Metric | Value | Reason |
|-|-|-|
| Attack Vector | Network | Internet accessible |
| Attack Complexity | Low | Easy to target |
| Privileges Required | None | No initial access required |
| User Interaction | None | Not required |
| Confidentiality | High | System data exposure |
| Integrity | High | System modification possible |
| Availability | High | Service disruption possible |


---

## Risk Explanation


Exposed administrative access significantly increases the possibility of unauthorized system compromise.


---

# Finding 003 — Excessive IAM Permissions


## Description


An identity contained more permissions than required for normal operations.


---

## CVSS Vector


```
CVSS:3.1/AV:N/AC:L/PR:L/UI:N/S:U/C:H/I:H/A:H
```


---

## Score


```
8.8
```


Severity:


```
High
```


---

## Metric Analysis


| Metric | Value | Reason |
|-|-|-|
| Attack Vector | Network | Cloud account access |
| Attack Complexity | Low | Exploitation is straightforward |
| Privileges Required | Low | Requires valid identity |
| User Interaction | None | Not required |
| Confidentiality | High | Sensitive resources accessible |
| Integrity | High | Resources can be modified |
| Availability | High | Services may be affected |


---

# Finding 004 — Missing Security Monitoring


## Description


The initial environment lacked centralized security monitoring capabilities.


---

## CVSS Vector


```
CVSS:3.1/AV:N/AC:H/PR:N/UI:N/S:U/C:L/I:L/A:L
```


---

## Score


```
5.3
```


Severity:


```
Medium
```


---

## Risk Explanation


Limited monitoring does not directly create compromise but reduces the ability to detect and respond to security incidents.


---

# 4. Vulnerability Summary


| ID | Finding | CVSS Score | Severity |
|-|-|-|-|
| VULN-001 | Public S3 Exposure | 7.5 | High |
| VULN-002 | SSH Exposure | 9.8 | Critical |
| VULN-003 | Excessive IAM Permissions | 8.8 | High |
| VULN-004 | Monitoring Gap | 5.3 | Medium |


---

# 5. Risk Prioritization


Priority order:


## Priority 1


```
SSH Exposure
CVSS 9.8
```


Immediate remediation required.


---

## Priority 2


```
IAM Permission Issue
CVSS 8.8
```


Reduce privilege exposure.


---

## Priority 3


```
Public S3 Exposure
CVSS 7.5
```


Protect cloud data.


---

## Priority 4


```
Monitoring Gap
CVSS 5.3
```


Improve visibility.


---

# 6. Final Assessment


CVSS analysis identified:


✓ One critical security exposure

✓ Two high-risk findings

✓ One medium-risk improvement area


Remediation activities significantly reduced the overall cloud security risk.


---

# Report Status


```
Completed
```