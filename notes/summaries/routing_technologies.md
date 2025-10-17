---
title: "Routing Technologies - TL;DR"
date: 2025-10-17
tags: [network, routing, static, dynamic, bgp, ospf, eigrp, fundamentals]
level: beginner
---

# Routing Technologies - TL;DR

**What**: Methods routers use to direct IP packets across networks, deciding the best path for data.  
**Why it matters**: Determines efficiency, scalability, and reliability of network communication.

---
## Static Routing
- Routes are **manually configured** by administrators.  
- Best for **small or stub networks**.  
- **Advantages**: simple setup, no protocol overhead, more secure.  
- **Disadvantages**: no automatic rerouting, hard to manage at scale.

---
## Dynamic Routing
- Routers **exchange routing info** automatically.  
- Updates routing tables in near real time.  
- **Advantages**: scalable, self-adjusting, less manual work.  
- **Disadvantages**: uses more CPU, memory, and bandwidth.  

---
## Dynamic Routing Protocols
- Share subnet info between routers.  
- Choose the **best path** using metrics (distance, cost, link state).  
- **Convergence time** varies by protocol.  
- Examples: **OSPF, EIGRP, BGP, RIP**.

---
## Enhanced Interior Gateway Routing Protocol (EIGRP)
- Cisco’s **hybrid** routing protocol (partly proprietary).  
- Fast convergence and loop-free operation.  
- Efficient bandwidth use and simple configuration.

---
## Open Shortest Path First (OSPF)
- **Link-state** protocol used within a single autonomous system.  
- Calculates routes based on link **costs** (throughput, delay, reliability).  
- **Load balances** across equal-cost paths.  
- Open standard supported by many vendors.

---
## Border Gateway Protocol (BGP)
- **Exterior** gateway protocol connecting different autonomous systems.  
- Backbone of the **Internet’s routing system**.  
- Focused on scalability and policy-based routing.  
- Uses **path attributes** to select the best routes globally.

---
## Routing Tables
- Each router keeps a **map of networks** and next hops.  
- The **most specific route** (longest prefix) wins.  
- When tied, administrative distance and metrics decide.  

---
## Administrative Distances
Used to prioritize routing sources:  
| Source | Distance |
|---------|-----------|
| Local | 0 |
| Static route | 1 |
| EIGRP | 90 |
| OSPF | 110 |
| RIP | 120 |
| DHCP default | 254 |
| Unknown | 255 |

---
## Routing Metrics
- Each protocol calculates cost differently.  
- Lower metric = preferred route.  
- Used to select between **redundant links**.

---
## First Hop Redundancy Protocol (FHRP)
- Creates a **virtual default gateway** (VIP).  
- If one router fails, another instantly takes over.  
- Ensures **continuous traffic flow** without manual reconfiguration.

---
## Subinterfaces
- Logical divisions of a physical interface (e.g., VLANs).  
- Useful for **trunking** and traffic segmentation.  
- Example:  
  - Ethernet1/1.10 → VLAN 10  
  - Ethernet1/1.20 → VLAN 20  

---
## Read More
- planned.
