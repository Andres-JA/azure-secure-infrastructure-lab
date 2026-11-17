# Azure Secure Infrastructure Lab

![Microsoft Azure](https://img.shields.io/badge/Microsoft_Azure-Cloud_Infrastructure-0078D4?logo=microsoftazure&logoColor=white)
![AZ-104](https://img.shields.io/badge/Certification-AZ--104-blue)
![Status](https://img.shields.io/badge/Status-In_Progress-yellow)

## Project Overview

This project focuses on designing, deploying, securing, and monitoring cloud infrastructure using **Microsoft Azure**.

The main objective is to gain hands-on experience with Azure administration services while preparing for the **Microsoft Azure Administrator (AZ-104)** certification.

The infrastructure will include virtual networks, Linux virtual machines, network security groups, storage services, monitoring, and resource governance.

The project is being developed using an **Azure for Students** subscription, with an emphasis on security best practices and cost optimization.

## Project Objectives

- Design and implement a secure Azure cloud infrastructure.
- Configure resource groups, virtual networks, and subnets.
- Deploy and manage Linux virtual machines.
- Implement network security using Network Security Groups (NSGs).
- Apply Azure Role-Based Access Control (RBAC).
- Monitor infrastructure using Azure Monitor.
- Manage cloud resources and optimize costs.
- Document the deployment process and technical decisions.

## Planned Architecture

The infrastructure will use the following network configuration:

| Resource | Configuration |
|---|---|
| Resource Group | `rg-az104-lab` |
| Virtual Network | `vnet-az104` |
| VNet Address Space | `10.0.0.0/16` |
| Web Subnet | `10.0.1.0/24` |
| Private Subnet | `10.0.2.0/24` |
| Operating System | Ubuntu Server 24.04 LTS |
| Cloud Provider | Microsoft Azure |

The architecture is designed to separate public-facing services from internal resources, providing better network isolation and security.

*Architecture diagram will be included as the infrastructure is implemented.*

## Project Roadmap

| Week | Focus Area | Status |
|---|---|---|
| Week 1 | Resource Governance & Azure Setup | In Progress |
| Week 2 | Virtual Networking & Security | Planned |
| Week 3 | Virtual Machines & Connectivity | Planned |
| Week 4 | Monitoring, Cost Management & Documentation | Planned |

---

## Week 1 — Azure Resource Governance & Initial Setup

### Objective

Establish the foundation of the Azure infrastructure by organizing cloud resources, understanding access control, and implementing basic cost management practices.

### Activities

**1. Azure Subscription**

- Reviewed the Azure for Students subscription.
- Identified subscription limitations and available credits.
- Explored the Azure Portal and resource management features.

**2. Resource Group**

Planned resource group: `rg-az104-lab`

Purpose:

- Organize related Azure resources.
- Simplify resource administration.
- Apply consistent resource governance.
- Facilitate cleanup after testing.

**3. Resource Tagging**

Defined the following tags:

| Tag | Value |
|---|---|
| Project | AZ104-Lab |
| Environment | Development |
| ManagedBy | AzurePortal |

Tags help organize resources and support cost analysis.

**4. Identity and Access Management**

Reviewed the fundamentals of:

- Microsoft Entra ID
- Azure Role-Based Access Control (RBAC)
- Azure resource scopes
- Principle of least privilege

**5. Cost Management**

Planned cost controls to monitor Azure credit consumption:

- Review Azure Cost Management.
- Configure budget alerts.
- Monitor resource consumption.
- Avoid unnecessary running virtual machines.

### Technical Decisions

| Decision | Justification |
|---|---|
| Single Resource Group | Simplifies resource organization and cleanup |
| Resource Tags | Improves resource tracking and cost visibility |
| Azure RBAC | Supports controlled access to resources |
| Budget Alerts | Helps prevent unexpected credit consumption |
| Small VM Sizes | Reduces infrastructure costs during testing |

### Evidence

Screenshots will be added after completing the corresponding activities.

Suggested evidence:

- Azure subscription overview
- Resource group configuration
- Resource tags
- RBAC access control
- Cost Management budget

---

##  Technologies

- Microsoft Azure
- Azure Resource Manager
- Microsoft Entra ID
- Azure RBAC
- Azure Cost Management
- Azure Virtual Network (planned)
- Azure Virtual Machines (planned)
- Azure Monitor (planned)
- Git & GitHub

##  Learning Outcomes

This project is intended to strengthen practical knowledge of Azure administration, including:

- Resource organization and governance
- Cloud infrastructure management
- Identity and access control
- Network security
- Monitoring and cost optimization

## References

- [Microsoft Learn — AZ-104](https://learn.microsoft.com/en-us/credentials/certifications/azure-administrator/)
- [Azure Resource Groups](https://learn.microsoft.com/en-us/azure/azure-resource-manager/management/manage-resource-groups-portal)
- [Azure RBAC](https://learn.microsoft.com/en-us/azure/role-based-access-control/overview)
- [Azure Cost Management](https://learn.microsoft.com/en-us/azure/cost-management-billing/)

---

**Project Status:** In Progress

*This is a personal hands-on learning project developed as part of my preparation for the Microsoft Azure Administrator (AZ-104) certification.*
