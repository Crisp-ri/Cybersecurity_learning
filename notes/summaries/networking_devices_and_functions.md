---
title: "Networking Devices and Functions — TL;DR"
date: 2025-09-24
tags: [network, fundamentals]
level: beginner
---

# Network Devices

**What**: Hardware used to connect, manage, and route traffic in a network (switches, routers, hubs, access points).
**Why it matters**: These devices control traffic flow, improve network performance, and ensure communication between devices locally and globally.

---
## Devices

- **Router** - routes traffic between IP subnets (Network layer, L3).
- **Switch** - forwards traffic based on MAC addresses (Data Link layer, L2).
- **Firewall** - filters traffic by IP, port, protocol, or application. Can operate on different layers: basic ones at L3/L4, advanced (Next-Gen) up to L7.
- **IDS (Intrusion Detection System) and IPS (Intrusion Prevention System)** - monitor network traffic. IDS alerts on suspicious activity, IPS can actively block it.
- **Load balancer** - distributes incoming traffic across multiple servers. Can work at L4 (transport level) or L7 (application level). Improves performance and provides fault tolerance.
- **Access Point** - extends a wired network to wireless clients (Data Link layer, L2).

---
## Functions

- **Content Delivery Network (CDN)** - geographically distributed caching servers, duplicate content, speed up delivery, transparent to users.
- **Virtual Private Network (VPN)** - encrypts traffic and creates a secure tunnel over a public network.
- **Quality of Service (QoS)** - traffic management policies to prioritize critical applications, control bandwidth, and reduce latency.
- **Domain Name System (DNS)** - resolves domain names into IP addresses.

---
## Key Mechanisms

- **Time To Live (TTL)** - an IP header field that decreases at each hop. When it reaches zero, the packet is dropped. Prevents routing loops.

---
## Read more
- planned.
