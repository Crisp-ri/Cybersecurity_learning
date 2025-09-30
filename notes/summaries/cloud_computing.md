---
title: "Cloud Computing - TL;DR"
date: 2025-09-27
tags: [cloud, fundamentals]
level: beginner
---

# Cloud Computing

**What:** a distributed collection of servers that host software and infrastructure.  
**Why it matters:** eliminates the need to purchase and maintain physical servers by providing access to services from cloud providers.  

---

## Designing the Cloud

### Network Function Virtualization (NFV)  
Virtualization of physical network devices.

- Managed via hypervisor.  
- Provides identical functionality to hardware devices.  
- Enables fast deployment and scaling of network functions.  
- Offers multiple deployment options.  

### Connection to the Cloud  
Mechanisms for connecting private resources to cloud environments.  

- **Virtual Private Cloud (VPC):** isolated pool of resources within a public cloud.  
- Multiple VPCs are common; connected via *Transit Gateway* (cloud router).  
- VPCs typically operate on separate IP subnets.  
- Connection to the cloud often established via VPN.  
- **NAT Gateway:** allows private subnets to reach external resources, blocks inbound access.  
- **VPC Endpoint:** provides direct connections between provider networks, bypassing the public internet.  

### Security: Groups and Lists
Control inbound and outbound traffic flows.

- **Control on Transport layer** - TCP or UDP port.
- **Control on Network layer** - Individual addresses, CIDR (Classless Inter-Domain Routing) block notation, IPv4 or IPv6.

#### Network security list (NSL)
1. Assign a security rule to an entire IP subnet.
2. Very broad - can become difficult to manage, not all devices in a subnet have same security posture.
3. More granularity may be needed (broad rules may not provide the right level of security).

#### Network security group (NSG)
1. Assign a security rule to a specific virtual NIC (VNIC). Applies to specific devices and network connections.
2. Different rules for devices in the same IP subnet.
3. Better control and granularity.

---
## Cloud Models

### Cloud Deployment Models
- **Public** - available to everyone over the Internet.
- **Private** - your own virtualized local data center.
- **Hybrid** - a mix of public and private.

### Software as a Service (SaaS)

- On-demand software (No local installation).
- Central management of data and applications.
- A complete application offering.
- **Example**: Gmail, Office 365.

### Infrastructure as a Service (IaaS) (Sometimes called Hardware as a Service (HaaS))

- Outsource your equipment.
- You're still responsible for the management and for security.
- Your data is out there but more within your control.
- **Example**: Web server providers.

### Platform as a Service (PaaS)

- No servers, no software, no maintenance team, no need for physical infrastructure management.
- Someone else handles the platform, you handle the development.
- You don't have direct control of the data, people, or infrastructure
- Put the building blocks together, develop your apps from what's available on the platform.
- **Example**: SalesForce.com.

---
## Read more
- planned.
