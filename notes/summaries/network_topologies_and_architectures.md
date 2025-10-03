---
title: "Network Topologies and Architectures - TL;DR"
date: 2025-10-03
tags: [network, fundamentals, topology, architecture, data-center]
level: beginner
---

# Network Topologies and Architectures

**What**: Logical and physical layouts that define how devices are connected and how data moves.  
**Why it matters**: Impacts performance, redundancy, troubleshooting, and cost.

---
## Topologies

- **Star / Hub-and-spoke** - most common in LANs, all devices connect to a central device (e.g. switch).
- **Mesh** - multiple links, can be fully or partially connected. Provides redundancy, fault tolerance, and load balancing. Used in WANs.
- **Hybrid** - mix of topologies. Most real networks are hybrids.
- **Spine and Leaf** - modern data center design. Each leaf connects to all spines; no leaf-to-leaf or spine-to-spine. Top-of-rack model.  
  - Advantages: simple cabling, redundancy, fast.  
  - Disadvantages: cost of additional switches.
- **Point-to-point** - simple one-to-one link. Mostly legacy (older WAN links, building-to-building connections).

---
## Architectures

- **Three-tier architecture**  
  - **Core** - central network layer (servers, DBs, apps).  
  - **Distribution** - intermediate layer managing access paths.  
  - **Access** - user connections (end devices, printers).  

- **Collapsed core**  
  - Two-tier model (Core + Distribution combined).  
  - Pros: simpler, cheaper, easier to manage.  
  - Cons: less resilient than full three-tier.

---
## Traffic Flows

- **East-West** - traffic inside the same data center, usually fast.  
- **North-South** - traffic in/out of the data center. Requires stricter security.

---
## Read more
- planned
