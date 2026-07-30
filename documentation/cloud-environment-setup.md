# Cloud Environment Setup Guide

## Enterprise Cloud Security Posture Assessment & Hardening Lab


---

# 1. Environment Overview


This document explains the deployment process used to create the AWS cloud security assessment environment.


The environment was designed to simulate an enterprise cloud infrastructure where security controls, monitoring services, and workloads can be evaluated.


---

# 2. Cloud Platform


## Provider


```
Amazon Web Services (AWS)
```


## Region


Example:

```
us-east-1
```


## Environment Type


```
Security Assessment Laboratory
```


---

# 3. Required Components


The environment contains:


| Component | Purpose |
|-|-|
| AWS Account | Cloud environment |
| IAM | Identity management |
| VPC | Network isolation |
| Subnet | Resource placement |
| EC2 | Compute workload |
| Security Groups | Firewall controls |
| S3 | Storage testing |
| CloudTrail | Audit logging |
| GuardDuty | Threat detection |
| Security Hub | Security posture monitoring |
| AWS Config | Configuration tracking |


---

# 4. AWS Account Preparation


## Step 1 — Secure Root Account


Actions:


- Enable Multi-Factor Authentication
- Avoid daily root account usage
- Create administrative IAM identity


Security Objective:


Protect the highest privilege account.


---

# 5. IAM Configuration


## Create IAM Administrator User


Configuration:


```
User Type:

IAM User
```


Permissions:


```
AdministratorAccess
```


Security improvements:


- Enable MFA
- Use strong authentication
- Avoid shared credentials


---

# 6. Create VPC Network


## VPC Configuration


Create:


```
VPC Name:

Enterprise-Security-VPC
```


CIDR:


```
10.0.0.0/16
```


Purpose:


- Network isolation
- Security boundary
- Resource organization


---

# 7. Create Subnet


## Public Subnet


Configuration:


```
Name:

Security-Public-Subnet
```


CIDR:


```
10.0.1.0/24
```


Purpose:


Hosts controlled internet-facing resources.


---

# 8. Configure Internet Gateway


Create:


```
Internet Gateway

Enterprise-IGW
```


Attach to:


```
Enterprise-Security-VPC
```


Purpose:


Provide external connectivity for public resources.


---

# 9. Configure Route Table


Create route:


```
Destination:

0.0.0.0/0


Target:

Internet Gateway
```


Purpose:


Allow controlled outbound internet communication.


---

# 10. Deploy EC2 Instance


## Instance Configuration


Example:


```
Name:

WebServer01
```


Operating System:


```
Amazon Linux 2023
```


Instance Type:


```
t2.micro
```


Purpose:


Simulate an enterprise workload.


---

# 11. Configure Security Group


Create:


```
WebServer-SecurityGroup
```


Inbound rules:


| Protocol | Port | Purpose |
|-|-|-|
| SSH | 22 | Administration |
| HTTP | 80 | Web Access |
| HTTPS | 443 | Secure Web Access |


Initial security testing included:


```
SSH Source:

0.0.0.0/0
```


This configuration was later remediated.


---

# 12. Create S3 Storage Resource


Create bucket:


```
enterprise-security-data
```


Security testing included:


- Access permissions
- Public exposure review
- Bucket policy analysis


Security controls:


- Block Public Access enabled
- Encryption enabled


---

# 13. Enable CloudTrail


Purpose:


Track AWS API activity.


Configuration:


```
Trail:

Enterprise-Security-Trail
```


Logging:


```
Enabled
```


Captured events:


- Console activity
- API calls
- Resource changes


---

# 14. Enable Amazon GuardDuty


Purpose:


Detect:


- Suspicious activity
- Credential abuse
- Malicious behavior


Configuration:


```
GuardDuty:

Enabled
```


---

# 15. Enable AWS Security Hub


Purpose:


Central security findings management.


Configuration:


```
Security Hub:

Enabled
```


Capabilities:


- Security posture evaluation
- Finding aggregation
- Compliance checks


---

# 16. Enable AWS Config


Purpose:


Track cloud configuration changes.


Configuration:


```
AWS Config:

Enabled
```


Monitored:


- Resource changes
- Security configurations
- Compliance state


---

# 17. Security Assessment Tools


The environment was assessed using:


## ScoutSuite


Purpose:


```
AWS security posture assessment
```


---

## Prowler


Purpose:


```
CIS AWS security benchmark evaluation
```


---

# 18. Environment Validation


Validation checks:


## Network


Verified:


✓ VPC created

✓ Subnet configured

✓ Internet connectivity available


---

## Compute


Verified:


✓ EC2 instance running

✓ Security groups attached


---

## Security Services


Verified:


✓ CloudTrail active

✓ GuardDuty active

✓ Security Hub active

✓ AWS Config active


---

# 19. Security Baseline


The completed environment follows:


- Least privilege principles
- Cloud logging best practices
- Network access restrictions
- Continuous security monitoring


---

# 20. Deployment Status


```
Completed
```


---

# Document Status


```
Completed
```