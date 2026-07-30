# MITRE ATT&CK Mapping Report

## Enterprise Cloud Security Posture Assessment & Hardening Lab


---

# 1. Purpose


This document maps identified cloud security risks and potential attacker activities to the MITRE ATT&CK Enterprise framework.


The purpose of this mapping is to:


- Understand attacker techniques
- Improve security detection
- Support threat hunting activities
- Recommend defensive controls


---

# 2. MITRE ATT&CK Overview


MITRE ATT&CK is a globally recognized knowledge base describing real-world adversary tactics and techniques.


Security teams use ATT&CK to:


- Analyze threats
- Develop detections
- Improve incident response
- Strengthen defenses


---

# 3. Cloud Security Detection Mapping


| Finding | ATT&CK Technique | Tactic |
|-|-|-|
| Public S3 Exposure | T1530 - Data from Cloud Storage | Collection |
| Internet Exposed SSH | T1133 - External Remote Services | Initial Access |
| Excessive IAM Permissions | T1078 - Valid Accounts | Defense Evasion / Persistence |
| Cloud Reconnaissance | T1580 - Cloud Infrastructure Discovery | Reconnaissance |
| Security Control Weakness | T1562 - Impair Defenses | Defense Evasion |


---

# 4. Technique Analysis


# T1530 — Data from Cloud Storage


## Tactic


```
Collection
```


## Description


Attackers may attempt to access sensitive information stored in cloud storage services.


## Related Finding


```
Public S3 Bucket Exposure
```


## Detection Opportunities


Monitor:


- Public bucket permissions
- Unusual object access
- Anonymous requests


## Defensive Recommendations


Implement:


- Block Public Access
- Bucket policy reviews
- CloudTrail monitoring


---

# T1133 — External Remote Services


## Tactic


```
Initial Access
```


## Description


Attackers may attempt to gain access through externally exposed remote services.


## Related Finding


```
Internet Exposed SSH
```


## Detection Opportunities


Monitor:


- Authentication failures
- Suspicious login attempts
- Unusual source locations


## Defensive Recommendations


Implement:


- IP allowlisting
- MFA
- Bastion hosts
- Private connectivity


---

# T1078 — Valid Accounts


## Tactic


```
Persistence
Defense Evasion
```


## Description


Attackers may use valid credentials to access cloud resources.


## Related Finding


```
Excessive IAM Permissions
```


## Detection Opportunities


Monitor:


- Unusual API activity
- Privilege changes
- New access keys


## Defensive Recommendations


Implement:


- Least privilege IAM
- MFA enforcement
- Access reviews


---

# T1580 — Cloud Infrastructure Discovery


## Tactic


```
Reconnaissance
```


## Description


Attackers may gather information about cloud infrastructure to identify possible targets.


## Detection Opportunities


Monitor:


- API enumeration
- Resource discovery attempts
- Unusual cloud queries


## Defensive Recommendations


Implement:


- IAM restrictions
- API monitoring
- CloudTrail analysis


---

# T1562 — Impair Defenses


## Tactic


```
Defense Evasion
```


## Description


Attackers may attempt to weaken security controls to avoid detection.


## Detection Opportunities


Monitor:


- Logging changes
- Security service modifications
- IAM permission changes


## Defensive Recommendations


Implement:


- Configuration monitoring
- Security alerts
- Administrative controls


---

# 5. Detection Coverage Matrix


| Technique | Detection Capability |
|-|-|
| T1530 | S3 Monitoring / CloudTrail |
| T1133 | Authentication Monitoring |
| T1078 | IAM Activity Monitoring |
| T1580 | Cloud Activity Analysis |
| T1562 | Security Configuration Monitoring |


---

# 6. Threat Hunting Opportunities


Security analysts should investigate:


## Unauthorized Cloud Storage Access


Search for:


```
Unexpected S3 object access
```


---

## Suspicious Authentication


Search for:


```
Multiple failed SSH attempts
```


---

## Privilege Abuse


Search for:


```
Unexpected IAM policy changes
```


---

## Cloud Reconnaissance


Search for:


```
Unusual API enumeration activity
```


---

# 7. Defensive Security Improvements


Based on ATT&CK analysis:


## Identity Protection


Recommended:


- MFA enforcement
- Least privilege access
- IAM monitoring


---

## Network Protection


Recommended:


- Private workloads
- Restricted inbound rules
- Network segmentation


---

## Cloud Visibility


Recommended:


- Centralized logging
- Threat detection
- Continuous monitoring


---

# 8. Final Assessment


The MITRE ATT&CK analysis demonstrates:


✓ Understanding of cloud attack techniques

✓ Ability to map findings to adversary behavior

✓ Detection engineering awareness

✓ Security improvement planning


---

# Document Status


```
Completed
```