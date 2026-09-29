# How to Pass Technical Screening Interviews for Microsoft Certified Azure Administrator (AZ-104)

> **A complete step-by-step masterclass on passing AZ-104 technical screening interviews, Azure RBAC governance, Virtual Network (VNet) peering, Storage redundancy, and App Service management.**

| Attribute | Details |
|---|---|
| **Category** | Exam & Interview Guide |
| **Reading Time** | 5 min read |
| **Published** | August 2026 |
| **Author** | [Careers.codes Editorial Team](https://www.linkedin.com/in/hasnain-ali-41aa042b9) |
| **Interactive Live Guide** | [Read on careers.codes](https://www.careers.codes/guides/how-to-pass-technical-screening-interviews-microsoft-certified-azure-administrator-az-104) |

## Overview

Master Azure RBAC roles, Management Groups, VNet Peering transit routing, Network Security Groups (NSG), Azure Storage redundancy (LRS/ZRS/GRS), and VMSS for AZ-104 interviews.

## Table of Contents

* [1. AZ-104 Exam & Azure Administrator Screening Scope](#1-az-104-exam-azure-administrator-screening-scope)
* [2. Azure RBAC Roles, Management Groups, & Policy Governance](#2-azure-rbac-roles-management-groups-policy-governance)
* [3. Virtual Network (VNet) Peering, NSGs, & User-Defined Routes](#3-virtual-network-vnet-peering-nsgs-user-defined-routes)
* [4. Azure Storage Redundancy (LRS, ZRS, GRS) & SAS Tokens](#4-azure-storage-redundancy-lrs-zrs-grs-sas-tokens)
* [5. Virtual Machine Scale Sets (VMSS) & Site Recovery (ASR)](#5-virtual-machine-scale-sets-vmss-site-recovery-asr)

---

## 1. AZ-104 Exam & Azure Administrator Screening Scope

The Microsoft Certified: Azure Administrator (AZ-104) certification validates expertise in implementing, managing, and monitoring identity, governance, storage, compute, and virtual networks on Azure.

1. **Manage Azure Identities & Governance (15–20% Weighting):** Entra ID users & groups, RBAC, Subscriptions, Management Groups, Azure Policy.
2. **Implement & Manage Storage (15–20% Weighting):** Storage accounts, Blob storage, Azure Files, Storage Explorer, SAS tokens, Backup/Recovery.
3. **Deploy & Manage Azure Compute Resources (20–25% Weighting):** ARM/Bicep templates, VMs, VM Scale Sets, Azure App Service, Azure Container Instances.
4. **Configure & Manage Virtual Networking (20–25% Weighting):** VNets, Subnets, VNet Peering, VPN Gateways, ExpressRoute, NSGs, Azure Load Balancer, Application Gateway.
5. **Monitor & Maintain Azure Resources (10–15% Weighting):** Azure Monitor, Network Watcher, Log Analytics workspaces, Alert rules.

## 2. Azure RBAC Roles, Management Groups, & Policy Governance

**Interview Scenario:** *"How do you structure Azure Management Groups, Subscriptions, and RBAC permissions for an enterprise with 50+ departments?"*

* **Management Group Hierarchy:** Create a root Management Group containing `Production`, `Staging`, and `Shared Services` child management groups. Attach Azure Policies at the Management Group level so governance rules automatically inherit to all child subscriptions.
* **Azure RBAC Custom Roles:** Define custom JSON roles specifying explicit `Actions` and `NotActions`:
  - **Owner:** Full access including role assignments.
  - **Contributor:** Full access excluding role assignments.
  - **Reader:** Read-only access to existing resources.

## 3. Virtual Network (VNet) Peering, NSGs, & User-Defined Routes

**Interview Scenario:** *"Explain how VNet Peering transit works and how Network Security Groups (NSG) evaluate traffic rules."*

* **VNet Peering:** Connects two VNets using Microsoft backbone network infrastructure. Non-transitive by default (if VNet A peers with VNet B, and VNet B peers with VNet C, VNet A CANNOT talk to VNet C unless gateway transit is enabled).
* **Network Security Group (NSG) Priority:** Evaluates inbound/outbound rules numerically from 100 to 4096. Lower numbers take precedence. As soon as a match occurs, rule processing stops.
* **User-Defined Routes (UDR):** Custom route tables that override default Azure system routing to force traffic through a Network Virtual Appliance (NVA) or Firewall.

## 4. Azure Storage Redundancy (LRS, ZRS, GRS) & SAS Tokens

**Interview Scenario:** *"Compare LRS, ZRS, and GRS storage redundancy options and explain Shared Access Signatures (SAS)."*

* **Locally Redundant Storage (LRS):** Replicates data 3 times within a single physical datacenter ($99.999999999\%$ / 11 9's durability).
* **Zone-Redundant Storage (ZRS):** Replicates data across 3 separate Availability Zones in the primary region ($12\text{ 9's}$ durability).
* **Geo-Redundant Storage (GRS):** Replicates data 3 times in primary region AND asynchronously replicates 3 copies to a paired secondary region 300+ miles away ($16\text{ 9's}$ durability).
* **Shared Access Signatures (SAS):** Provides granular, time-limited delegated access to Blob/Table resources without exposing storage account access keys.

## 5. Virtual Machine Scale Sets (VMSS) & Site Recovery (ASR)

**Interview Scenario:** *"How do Azure Virtual Machine Scale Sets (VMSS) handle automatic horizontal scaling during sudden web traffic spikes?"*

1. **Auto-Scaling Metrics:** Define autoscale settings based on Average CPU Utilization > 75% for 10 minutes to scale OUT (add instances) or CPU < 25% to scale IN.
2. **Health Probes & Repair:** VMSS monitors VM instance health using Application Health Extensions. Unhealthy VM instances are automatically destroyed and replaced.
3. **Azure Site Recovery (ASR):** Replicates entire VM workloads to a paired secondary Azure region for automated Disaster Recovery failover.

---

### 🔗 Explore More Developer Resources

* **Live Platform:** [careers.codes](https://www.careers.codes)
* **All Guides:** [careers.codes/guides](https://www.careers.codes/guides)
* **Curator:** [Hasnain Ali on LinkedIn](https://www.linkedin.com/in/hasnain-ali-41aa042b9) & [X (Twitter)](https://x.com/HasnainAlijutt6)
