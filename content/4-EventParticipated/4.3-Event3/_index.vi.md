---
title: "Event 3"

weight: 1
chapter: false
pre: " <b> 4.2. </b> "
---



# Summary Report: “AWS Well-Architected Framework – Security Pillar Workshop”

### Event Objectives

- Deep-dive into the Security Pillar of the AWS Well-Architected Framework

- Understand modern security best practices: Least Privilege, Zero Trust, Defense in Depth

- Learn how to design secure cloud environments with Identity, Detection, Infrastructure Protection, Data Protection, and Incident Response pillars


### Key Highlights

#### Security Foundation

- Explained the role of the Security Pillar within the Well-Architected Framework  
- Core principles:

Least Privilege — minimize access permissions

Zero Trust — never trust, always verify

Defense in Depth — layered security approach

- Review of the Shared Responsibility Model and how it applies to AWS services
-  Overview of common cloud threats in Vietnam, including misconfigurations, credential compromise, and public-data exposure

#### Pillar 1 — Identity & Access Management (IAM)

**Modern IAM Architecture:**

- IAM concepts: Users, Roles, Policies, and avoiding long-term credentials

- Identity modernization with IAM Identity Center (SSO, permission sets)

- Governance for multi-account environments via Service Control Policies (SCP) and permission boundaries

- Strengthening access control with MFA, credential rotation, and Access Analyzer

- Mini Demo: IAM Policy validation and access simulation

#### Pillar 2 — Detection

**Detection & Continuous Monitoring:**

- Unified logging and monitoring using:

CloudTrail (organization-level)

GuardDuty threat detection

Security Hub compliance findings

- Logging across all layers: VPC Flow Logs, ALB logs, S3 Access Logs

- Automated alerting with EventBridge

- Concept of Detection-as-Code for repeatable and auditable monitoring rules

#### Pillar 3 — Infrastructure Protection

**Network & Workload Security:**

- Designing secure networks with VPC segmentation and correct use of public vs private subnets

- Comparison of Security Groups vs NACLs with recommended patterns

- Layers of perimeter defense: AWS WAF, Shield, Network Firewall

- Workload-level protection for EC2, ECS, and EKS environments

#### Pillar 4 — Data Protection

**Encryption, Keys & Secrets:**

- Deep dive into AWS KMS: key policies, grants, rotation strategies

- Encryption best practices for AWS services (S3, EBS, RDS, DynamoDB)

- Managing sensitive configuration with Secrets Manager and Parameter Store

- Data classification and guardrails aligned with compliance and governance needs
#### Pillar 5 — Incident Response

- AWS Incident Response lifecycle

- Walkthrough of key playbooks:

Compromised IAM key containment

S3 public exposure remediation

EC2 malware detection response steps

- Techniques for snapshot creation, resource isolation, and evidence collection

- Automated IR workflows using Lambda and Step Functions

#### Wrap-Up & Q&A
- Summary of all 5 Security Pillars

- Discussion on common pitfalls in Vietnamese cloud deployments

- Recommended learning path:

AWS Security Specialty

AWS Solutions Architect Professional

### Key Takeaways

#### Security Design Mindset

Security must be built from the foundation, not added later

Consistent enforcement of least privilege and strong identity controls

Visibility is essential—log everything, monitor continuously

#### Technical Implementation

Adopt centralized identity with IAM Identity Center

Use organization-wide logging and threat detection tools

Apply network segmentation and layered protection for workloads

Implement encryption, key management, and secret rotation systematically

#### Operational Excellence

Build repeatable incident response playbooks

Automate detection and remediation where possible

Establish governance practices across multi-account AWS environments

### Applying to Work

Review and refactor existing IAM structure following modern IAM patterns

Introduce organization-level CloudTrail and centralized logging

Strengthen infrastructure controls with VPC segmentation + WAF/Shield

Implement encryption standards and secret rotation policies

Build IR playbooks and integrate automation into response workflows

### Event Experience

Attending this workshop provided a structured, comprehensive, and practical understanding of AWS cloud security. Key reflections include:

#### Learning from highly skilled speakers
In-depth guidance from AWS security specialists

Real-world examples of cloud security incidents in Vietnam

#### Hands-on demonstrations
Practical IAM policy simulation

Step-by-step examples of threat detection and IR automation

#### Strategic mindset shift
Understanding that security is not only technical—it requires governance, culture, and continuous improvement

#### Networking opportunities
Engaging discussions with AWS experts and peers on real security challenges faced by enterprises



> Overall, this workshop strengthened both my technical skills and strategic understanding of cloud security, helping me design more secure, resilient, and compliant architectures.
