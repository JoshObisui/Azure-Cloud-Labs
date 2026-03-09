# Azure-Cloud-Labs
Hands-on Azure cloud administration labs demonstrating identity management, networking, virtual machines, monitoring, and security operations.

# Azure Cloud Administration Labs

## Overview

This repository contains hands-on Microsoft Azure labs focused on cloud infrastructure, identity management, networking, and security monitoring. These labs were completed to strengthen practical cloud administration skills aligned with the Microsoft Certified: Azure Administrator Associate (AZ-104).

The goal of these labs is to simulate real-world enterprise cloud environments while demonstrating secure infrastructure deployment and monitoring.

---

## Technologies Used

* Microsoft Azure
* Microsoft Entra ID
* Azure Virtual Machines
* Azure Virtual Network
* Azure Monitor
* Microsoft Sentinel
* Windows Server 2022

---

# Lab 1 – Azure Identity and Access Management

## Overview

This lab demonstrates identity administration using Microsoft Entra ID in Microsoft Azure. The objective was to simulate common enterprise identity management tasks including user creation, group management, and role-based access control.

Identity is the core security boundary in cloud environments, and proper configuration of users and permissions ensures secure access to cloud resources.

---

## Lab Objectives

* Create Azure users
* Configure security groups
* Assign RBAC permissions
* Enable identity security defaults

---

## User Creation

Users were created in Microsoft Entra ID to simulate an enterprise environment with multiple roles.

Example users created:

| User            | Role                |
| --------------- | ------------------- |
| Joshua          | Administrator       |
| Aubrey          | IT Support          |
| Dwayne          | IT support          |
| Johran          | IT support          |

### Screenshot – Azure Users


---

## Security Group Configuration

Security groups were created to logically organize users and simplify role assignment.

Groups created:

* CloudAdmins
* ITSupport

### Screenshot – Security Groups


---

## RBAC Role Assignment

RBAC roles were assigned at the subscription level to enforce least-privilege access.

Example configuration:

* CloudAdmins → Contributor
* ITSupport → Reader

### Screenshot – RBAC Role Assignment



---

## Security Implementation

Security defaults were enabled to enforce multi-factor authentication for administrative accounts.

This provides:

* MFA enforcement
* identity protection
* secure login policies

---

## Skills Demonstrated

* Azure identity administration
* RBAC access control
* security policy enforcement
* user lifecycle management
---

# Lab 2 – Azure Virtual Network and Virtual Machine

## Objective

Deploy a cloud infrastructure environment with networking and a Windows Server virtual machine.

## Key Tasks

* Created a Resource Group
* Designed Azure Virtual Network with segmented subnets
* Configured Network Security Group rules
* Deployed Windows Server 2022 VM
* Secured RDP access

## Network Architecture

Virtual Network: 10.0.0.0/16

Subnets:

* WebSubnet (10.0.1.0/24)
* AdminSubnet (10.0.2.0/24)

## Skills Demonstrated

* Cloud networking
* VM deployment
* Secure infrastructure design


---

# Lab 3 – Cloud Monitoring and Security (Sentinel)

## Objective

Implement centralized monitoring and security analytics using Azure Monitor and Microsoft Sentinel.

## Key Tasks

* Created Log Analytics workspace
* Connected Azure Virtual Machine to logging
* Queried logs using KQL
* Enabled Microsoft Sentinel
* Created an analytics detection rule

Example query used:

```
Heartbeat
| take 10
```

## Skills Demonstrated

* Cloud monitoring
* Log analytics
* Security event detection
* SIEM configuration

---

# Skills Demonstrated

* Azure infrastructure deployment
* Cloud security monitoring
* Network segmentation
* Identity and access management
* Security analytics

---

# Author

Joshua Obisui
Cybersecurity Graduate | Cloud & Security

Certifications:

* Microsoft Certified: Azure Administrator Associate (AZ-104)
* CompTIA Security+
