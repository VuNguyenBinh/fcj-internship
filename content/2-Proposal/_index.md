---
title: "Proposal"
date: 2025-09-11
weight: 2
chapter: false
pre: " <b> 2. </b> "
---


# AWS Security Scan Project  
## A CI/CD Automation Solution Integrating Security Analysis and System Safety Monitoring

### 1. Executive Summary  
The **AWS Security Scan Project** is designed to automate security inspection throughout the software development lifecycle by integrating AWS services such as **CodePipeline**, **CodeBuild**, **CodeGuru Reviewer**, and **AWS Security Hub**.  
The project aims to assist DevOps teams or DevSecOps students in implementing a CI/CD pipeline capable of **early vulnerability detection, automated alerts, and real-time security reporting**.

### 2. Problem Statement  
*Current Challenges*  
In many software projects, the CI/CD process often focuses only on build and deployment while **lacking automated security control**. Vulnerabilities are usually discovered after deployment, resulting in wasted time and potential system risks.

*Proposed Solution*  
Integrate “Security Scan as Code” into an automated pipeline:
- **CodePipeline** orchestrates the full build–scan–deploy workflow.  
- **CodeBuild** executes source code scans and performs security testing.  
- **CodeGuru Reviewer** conducts static code analysis to detect bugs and security issues.  
- **AWS Security Hub** and **Amazon Detective** centralize alerts and aggregate data from **CloudWatch**, **GuardDuty**, and **CloudTrail**, allowing administrators to identify potential system-wide threats.  

All code changes are automatically scanned, and any abnormal findings trigger notifications via **Amazon SNS**.

### 3. Solution Architecture  
The pipeline consists of **five main stages**: development, build, security scanning, deployment, and monitoring.


*AWS Services Used:*  
- **GitLab**: Acts as the source repository and triggers the pipeline upon each new commit.  
- **AWS CodePipeline**: Automates the CI/CD workflow.  
- **AWS CodeBuild**: Builds the application and runs security testing tools (e.g., SonarQube, Trivy, Bandit).  
- **AWS CodeGuru Reviewer**: Performs AI-powered code reviews to identify issues and suggest improvements.  
- **AWS Security Hub**: Centralizes vulnerability findings and compliance checks.  
- **Amazon Detective**: Analyzes logs and detects suspicious activities.  
- **Amazon CloudWatch** and **AWS GuardDuty**: Provide continuous monitoring and threat detection.  
- **Amazon SNS**: Sends alerts when vulnerabilities or anomalies are detected.  

This architecture ensures continuous integration of security controls, automated analysis, and centralized incident visibility across all development stages.

### 4. Expected Outcomes  
- **Security-first CI/CD Pipeline**: Embeds automated scanning and analysis into every commit.  
- **Improved Efficiency**: Reduces manual security testing workload.  
- **Enhanced Visibility**: Centralized dashboards and real-time alerts improve system awareness.  
- **Practical Learning Resource**: Serves as a DevSecOps study case for security automation using AWS services.  

---


