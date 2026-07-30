# Cloud Security Risk Register

## Enterprise Cloud Security Posture Assessment & Hardening Lab


---

# 1. Risk Register Overview


This document tracks security risks identified during the AWS cloud security assessment.


The purpose of this register is to:


- Document security weaknesses
- Prioritize remediation activities
- Track risk reduction
- Support security decision-making


---

# 2. Risk Assessment Methodology


Risk was evaluated using:


## Likelihood


The probability that a threat could successfully exploit the weakness.


Ratings:


- Low
- Medium
- High


---

## Impact


The potential business damage caused by successful exploitation.


Ratings:


- Low
- Medium
- High
- Critical


---

## Risk Rating


Risk level is calculated based on:


```
Risk = Likelihood × Impact
```


---

# 3. Risk Summary


| ID | Finding | Asset | Severity | Status |
|-|-|-|-|-|
| RISK-001 | Public S3 Bucket Exposure | S3 Storage | Critical | Remediated |
| RISK-002 | Internet Exposed SSH | EC2 Security Group | High | Remediated |
| RISK-003 | Excessive IAM Permissions | IAM Identity | High | Remediated |
| RISK-004 | Limited Security Monitoring | Cloud Environment | Medium | Remediated |


---

# 4. Detailed Risk Analysis


# RISK-001 — Public S3 Bucket Exposure


## Description


An S3 bucket was configured with public accessibility, allowing unauthorized external access.


---

## Affected Asset


```
enterprise-public-data S3 Bucket
```


---

## Threat Scenario


An attacker could discover the exposed bucket and access stored information without authorization.


---

## Likelihood


```
High
```


Reason:


- Internet accessible resource
- No authentication required


---

## Impact


```
Critical
```


Potential impact:


- Data exposure
- Privacy violations
- Compliance issues


---

## Risk Rating


```
Critical
```


---

## Remediation Status


```
Completed
```


Actions:


- Enabled Block Public Access
- Removed public bucket permissions
- Reviewed bucket policy


---

# RISK-002 — Internet Exposed SSH Access


## Description


The EC2 security group allowed SSH connections from all internet addresses.


---

## Affected Asset


```
WebServer01 EC2 Instance
```


---

## Threat Scenario


Attackers could perform reconnaissance and attempt unauthorized remote access.


---

## Likelihood


```
High
```


---

## Impact


```
High
```


Potential impact:


- Unauthorized access attempts
- Account compromise
- Server compromise


---

## Risk Rating


```
High
```


---

## Remediation Status


```
Completed
```


Actions:


- Restricted SSH source addresses
- Removed unnecessary exposure
- Applied network security controls


---

# RISK-003 — Excessive IAM Permissions


## Description


An identity contained permissions beyond operational requirements.


---

## Affected Asset


```
IAM SecurityAuditor User
```


---

## Threat Scenario


Compromised credentials could allow excessive cloud resource access.


---

## Likelihood


```
Medium
```


---

## Impact


```
High
```


---

## Risk Rating


```
High
```


---

## Remediation Status


```
Completed
```


Actions:


- Applied least privilege
- Removed unnecessary permissions
- Reviewed IAM policies


---

# RISK-004 — Limited Security Monitoring


## Description


Initial environment lacked centralized cloud security visibility.


---

## Affected Asset


```
AWS Cloud Environment
```


---

## Threat Scenario


Security events could occur without timely detection.


---

## Likelihood


```
Medium
```


---

## Impact


```
Medium
```


---

## Risk Rating


```
Medium
```


---

## Remediation Status


```
Completed
```


Actions:


- Enabled CloudTrail
- Enabled GuardDuty
- Enabled Security Hub
- Enabled AWS Config


---

# 5. Risk Priority Matrix


| Risk | Severity | Priority |
|-|-|-|
| Public S3 Exposure | Critical | P1 |
| SSH Exposure | High | P2 |
| IAM Permissions | High | P2 |
| Monitoring Gap | Medium | P3 |


---

# 6. Risk Treatment Summary


| Risk ID | Treatment |
|-|-|
| RISK-001 | Mitigate |
| RISK-002 | Mitigate |
| RISK-003 | Mitigate |
| RISK-004 | Mitigate |


---

# 7. Final Risk Assessment


After remediation:


✓ Critical exposure removed

✓ Attack surface reduced

✓ Security visibility improved

✓ Identity controls strengthened


---

# Document Status


```
Completed
```