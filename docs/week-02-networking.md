# Week 2 - Virtual Networking and Security

## Objective

Build the network foundation for a public web workload and a private application/database workload. Separate subnets provide the structure for applying different network security policies.

**Part 1 scope:** virtual network, IP address planning, and subnet creation. NSG rules and their validation will be documented in the second part.

## 1. Virtual Network

Created **`vnet-az104`** in **`rg-az104-lab`** with the address space **`10.0.0.0/16`**. The current overview shows the VNet in **North Central US**, under the Azure for Students subscription.

The address range accommodates separate workload subnets and leaves room for additional network segments as the lab grows.

![VNet overview showing vnet-az104, the 10.0.0.0/16 address space, and North Central US](../screenshots/2.1-vnet-address-space.png)

## 2. Web Subnet

Created the web subnet with **`10.0.1.0/24`** for the Linux web VM. In the expanded application design, this VM hosts Nginx and the Flask/Gunicorn application that connects to PostgreSQL over the private network.

The creation screenshot records the subnet as **`subnet-web`**. Keeping the web tier in its own subnet provides a separate scope for its HTTP and administrative access rules.

![Subnet creation confirmation showing subnet-web with the 10.0.1.0/24 range](../screenshots/2.2-subnet-web.png)

## 3. Private Subnet

Created **`snet-private`** with **`10.0.2.0/24`** for the internal Linux VM, which now hosts PostgreSQL. The intended design keeps that VM without a public IP and permits database access from the web VM through an explicit NSG rule.

| Subnet shown in the creation evidence | Address range | Role |
|---|---|---|
| `default` | `10.0.0.0/24` | Default subnet present in the VNet |
| `subnet-web` | `10.0.1.0/24` | Web and application tier |
| `snet-private` | `10.0.2.0/24` | Private PostgreSQL tier |

![Subnet list showing the default, web, and private subnets with non-overlapping address ranges](../screenshots/2.3-subnets-web-and-private.png)

The subnet screenshots capture the initial configuration, before NSG associations were visible. **Separate subnets alone do not enforce traffic isolation**; the NSG rules covered in the next part define which connections are allowed or denied.

## Progress

The VNet and both workload subnets are recorded with non-overlapping address ranges. The second part will document the web and private NSGs, rule priorities, and subnet associations.

[Back to project overview](../README.md)
