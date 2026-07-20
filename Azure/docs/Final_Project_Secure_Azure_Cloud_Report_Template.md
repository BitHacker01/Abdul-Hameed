# Final Project: Design and Implementation of a Secure Azure Cloud Environment

## Cover Page

**Project Title:** Design and Implementation of a Secure Azure Cloud Environment

**Organization:** ABC Technologies

**Role:** Cloud Security Engineer

**Platform:** Microsoft Azure

**Author:** ____________________

**Date:** ______________________

---

# Executive Summary

This project demonstrates the design, deployment, hardening, monitoring, and assessment of a secure Microsoft Azure cloud environment for **ABC Technologies**. The implementation follows Azure security best practices by applying preventive, detective, and monitoring security controls across compute, storage, identity, and monitoring services.

The project includes:

- Secure Linux Virtual Machine deployment
- Azure RBAC implementation
- Secure Azure Storage configuration
- Azure Monitor and Log Analytics
- Microsoft Sentinel SIEM integration
- Just-In-Time (JIT) VM Access
- Vulnerability Assessment using Nmap
- Security Assessment Report

---

# Project Objectives

- Deploy and secure Azure resources
- Implement RBAC using the Principle of Least Privilege
- Secure Azure Storage with SAS Tokens and Network Restrictions
- Configure Azure Monitor
- Configure Microsoft Sentinel
- Implement Just-In-Time VM Access
- Perform vulnerability assessment using Nmap
- Produce security documentation and architecture diagram

---

# Architecture Diagram

> Insert architecture diagram here.

The architecture should include:

- Azure Subscription
- Resource Group
- Linux Virtual Machine
- Network Security Group (NSG)
- Storage Account
- Private Blob Container
- SAS Access
- Azure Monitor
- Log Analytics Workspace
- Microsoft Sentinel
- RBAC Users
- Defender for Cloud (JIT)

---

# Task 1 – Secure Virtual Machine Deployment

## Objective

Deploy and secure a Linux Virtual Machine.

## Implementation

- Create Linux VM
- Configure SSH on Port **2244**
- Configure NSG
- Allow only required inbound ports
- Verify SSH connectivity

## Evidence

- VM Deployment Screenshot
- NSG Rules Screenshot
- SSH Connection Screenshot

## Observations

(Add your observations)

---

# Task 2 – Identity and Access Management (RBAC)

## Objective

Implement Role-Based Access Control.

### User 1 – VM Administrator

Role:

- Virtual Machine Contributor

Responsibilities

- Start VM
- Stop VM
- Modify VM Settings

### User 2 – Storage Administrator

Role:

- Storage Blob Data Contributor

Responsibilities

- Upload blobs
- Download blobs
- Generate SAS Tokens

## Validation

- VM Admin cannot manage Storage
- Storage Admin cannot manage VM
- Principle of Least Privilege verified

## Evidence

- User Creation
- Role Assignment
- Access Validation

---

# Task 3 – Secure Storage Configuration

## Objective

Secure Azure Blob Storage.

## Configuration

- Storage Account
- Private Blob Container
- Upload Sample Files
- Disable Public Access
- Generate SAS Token
- Configure IP Restrictions

## Validation

- Public Access Blocked
- SAS URL Working
- Unauthorized IP Blocked

## Evidence

- Storage Screenshots
- SAS Demonstration
- Network Restriction Screenshots

---

# Task 4 – Azure Monitor

## Components

- Azure Monitor
- Log Analytics Workspace
- VM Insights

## Dashboard

Include

- CPU Usage
- Memory Usage
- Network Traffic
- Disk Activity

Visualization

- Line Chart
- Gauge
- Single Value

## Validation

Generate CPU load and verify dashboard updates.

## Evidence

- Azure Monitor
- Dashboard
- CPU Utilization

---

# Task 5 – Microsoft Sentinel

## Configuration

- Log Analytics Workspace
- Microsoft Sentinel
- Syslog Collection

## Threat Scenario

Generate multiple failed SSH login attempts.

## Alert Rule

Trigger alert when:

- Failed SSH Logins > 5

## Validation

- Failed Login Logs
- KQL Query
- Alert / Incident

## Evidence

- Sentinel Configuration
- KQL Query
- Alert Screenshot

---

# Task 6 – Just-In-Time (JIT) Access

## Objective

Implement temporary administrative access.

## Configuration

- Enable JIT
- Protect Port 80
- Request Temporary Access

## Validation

- Access Approved
- Port Automatically Closed

## Evidence

- JIT Configuration
- Access Request
- Expiration Screenshot

---

# Task 7 – Vulnerability Assessment

## Tool

Nmap

## Assessment

- Identify Open Ports
- Detect Running Services
- Analyze Attack Surface

## Findings

| Open Port | Service | Risk | Recommendation |
|-----------|----------|------|----------------|
| | | | |

## Evidence

- Nmap Scan
- Service Enumeration
- Findings Summary

---

# Task 8 – Security Assessment Report

## Risks Identified

- Open Services
- Weak Configurations
- Access Control Issues
- Public Exposure Risks

## Security Controls Implemented

- RBAC
- NSG Rules
- Custom SSH Port
- Private Blob Storage
- SAS Token
- IP Restriction
- Azure Monitor
- Microsoft Sentinel
- JIT Access

## Recommendations

- Enable MFA
- Enable Defender for Cloud
- Use Private Endpoints
- Enable Backup
- Enable Azure Policy
- Configure Update Management
- Enable Microsoft Defender for Storage

---

# Conclusion

The project successfully demonstrates a secure Azure cloud environment implementing preventive, detective, and monitoring controls. Security best practices were applied across identity, networking, storage, monitoring, and threat detection to improve the overall security posture of the Azure infrastructure.

---

# References

- Microsoft Learn
- Azure Security Benchmark
- Microsoft Defender for Cloud Documentation
- Microsoft Sentinel Documentation
- Azure Monitor Documentation
