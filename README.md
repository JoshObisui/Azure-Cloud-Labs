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
| Johran          | Administrator       |
| Dwayne          | IT support          |
| Aubrey          | IT support          |

### Screenshot – Azure Users
![image alt](https://github.com/JoshObisui/Azure-Cloud-Labs/blob/af698a40eef9c5ed8947a65d3fb4f9e3519721a0/Lab%201/Lab%201%20Images/AzUsers.png)

---

## Security Group Configuration

Security groups were created to logically organize users and simplify role assignment.

Groups created:

* CloudAdmins
* ITSupport

### Screenshot – Security Groups
![image alt](https://github.com/JoshObisui/Azure-Cloud-Labs/blob/b1ec00b499f5b206c83b326935744132b2a62e96/Lab%201/Lab%201%20Images/AZGroups.png)

---

## RBAC Role Assignment

RBAC roles were assigned at the subscription level to enforce least-privilege access.

Example configuration:

* CloudAdmins → Contributor
* ITSupport → Reader

### Screenshot – RBAC Role Assignment
![image alt](https://github.com/JoshObisui/Azure-Cloud-Labs/blob/71693af3a9c0d3496dff336e20ab89d0c3e35e78/Lab%201/Lab%201%20Images/CloudAdminRBAC.png)

![image alt](https://github.com/JoshObisui/Azure-Cloud-Labs/blob/4d3eecafeee8345c572c6995551fe06eb78e13fa/Lab%201/Lab%201%20Images/ITRBAC.png)

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

# Lab 2 – Azure Virtual Network and Virtual Machine Deployment

## Overview

This lab demonstrates deployment of cloud infrastructure within Microsoft Azure including networking, subnet segmentation, and virtual machine provisioning.

The environment simulates a typical enterprise cloud architecture.

---

## Infrastructure Architecture

Virtual Network Address Space:

10.0.0.0/16

Subnets:

| Subnet      | Address Range |
| ----------- | ------------- |
| WebSubnet   | 10.0.1.0/24   |
| AdminSubnet | 10.0.2.0/24   |

---

## Virtual Network Deployment

A Virtual Network was created to isolate cloud resources and enable network segmentation.

### Screenshot – Virtual Network

![image alt](https://github.com/JoshObisui/Azure-Cloud-Labs/blob/e72a18ec7f6be5dc99eb1f32c45e109d29e644c5/Lab2/AzVnets.png)

![image alt](https://github.com/JoshObisui/Azure-Cloud-Labs/blob/e1e6cbee84be5915a842cedc2f5fa6a0f0ae16d8/Lab2/Topology.png)

---

## Network Security Group

A Network Security Group was configured to control inbound traffic to the VM.

Inbound rule created:

* Allow RDP (3389)
* Source restricted to administrator IP

### Screenshot – NSG Rules

![image alt](https://github.com/JoshObisui/Azure-Cloud-Labs/blob/b0ec46355d8bdc4ce63826cfa5eb985b0b337db4/Lab2/AzNSG.png)

---

## Virtual Machine Deployment

A Windows Server virtual machine was deployed in the AdminSubnet.

VM Configuration:

* Image: Windows Server 2022
* Size: B1s
* Network: AdminSubnet
* Secure RDP access

### Screenshot – VM Deployment

![image alt](https://github.com/JoshObisui/Azure-Cloud-Labs/blob/60329601f80a26f595cd590440396116b5fb8306/Lab2/VMDeployment1.png)

---

## Skills Demonstrated

* Azure networking architecture
* subnet segmentation
* secure VM deployment
* network access control


---

# Lab 3 – Azure Monitoring and Security Analytics

## Overview

This lab focuses on monitoring and security analytics using Azure Monitor, Log Analytics Workspace, and Microsoft Sentinel.

Centralized logging enables organizations to monitor infrastructure health and detect security threats.

---

## Log Analytics Workspace

A Log Analytics Workspace was created to collect telemetry from Azure resources.

### Screenshot – Log Analytics Workspace

![image alt](https://github.com/JoshObisui/Azure-Cloud-Labs/blob/d231f3ff7e05da1b0713bae6ee28dd2359a7fa8a/Lab%203/Cloud%20Logs.png)

---

## Connecting VM to Logging

The Azure virtual machine was connected to the workspace using the Azure Monitor Agent.

This enables telemetry collection including:

* system performance
* security logs
* resource health

### Screenshot – VM Connected to Logs

![image alt](https://github.com/JoshObisui/Azure-Cloud-Labs/blob/36f1ddd9edf8fa1fb6e1f10c8f87c7da2739b1b4/Lab%203/Alert%20Rules.png)

---

## Querying Logs

Logs were queried using Kusto Query Language to verify successful telemetry ingestion.

Example query:

```kql
Heartbeat
| take 10
```

### Screenshot – Log Query Results

![image alt](https://github.com/JoshObisui/Azure-Cloud-Labs/blob/8ad86607120a570f4f0727acde72a4c353f6afed/Lab%203/Cloud%20Heartbeat.png)

---

## Microsoft Sentinel Integration

Microsoft Sentinel was enabled on the workspace to provide SIEM functionality.

An analytics rule was created to detect potential failed login attempts.

### Screenshot – Sentinel Dashboard

![image alt](https://github.com/JoshObisui/Azure-Cloud-Labs/blob/90a92044aeff5cad3a1cc2257cbfc10b1860ee87/Lab%203/Analytic%20Rule.png)

---

## Skills Demonstrated

* centralized cloud monitoring
* log analytics using KQL
* security event detection
* SIEM configuration


---

# Author

Joshua Obisui
Cybersecurity Graduate | Cloud & Security

Certifications:

*CompTIA Security+
* Microsoft Certified: Azure Administrator Associate (AZ-104) 
* Microsoft Azure Fundamentals (AZ900)
* Microsoft Security, Compliance, Identity Fundamentals (SC900)	
