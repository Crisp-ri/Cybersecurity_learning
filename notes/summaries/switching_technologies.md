---
title: "VLANs and Trunking - TL;DR"
date: 2025-10-29
tags: [networking, vlan, trunking, stp]
level: beginner
---

# VLANs and Trunking

**What:** Virtual segmentation and interconnection of local networks.  
**Why it matters:** Increases efficiency, security, and flexibility of LAN management.  

---

## LANs
**Local Area Network (LAN):**  
A group of devices in the same broadcast domain.

---

## Virtual LANs (VLANs)
**Virtual Local Area Networks:**  
Logical separation of devices within the same physical infrastructure.

- Defined and named within the switch’s VLAN database.  
- Example:  
  - VLAN 1: Gate room  
  - VLAN 2: Dialing room  
  - VLAN 3: Infirmary  

---

## 802.1Q Trunking
**What it does:** Adds a VLAN tag inside Ethernet frames to identify traffic between VLANs.

**Frame structure:**  
Preamble - SFD - Destination MAC - Source MAC - VLAN - Type - Payload - FCS

- VLAN ID: 12 bits → 4,094 possible VLANs.  
- Normal range: 1–1005 | Extended range: 1006–4094.  
- VLAN 0 and 4095 are reserved.  
- Legacy ISL (Inter-Switch Link) is obsolete — everyone uses 802.1Q.

---

## Native VLAN
**Default VLAN vs. Native VLAN:**

- Default VLAN → automatically assigned to interfaces.  
- Native VLAN → carries untagged frames over a trunk.  

**Key points:**
- Must match between switches.  
- Used for devices that can’t handle 802.1Q tagging.  
- Mismatched native VLANs cause switch alerts.

---

## Layer 3 Switches
**What they are:**  
A hybrid device that performs both switching (Layer 2) and routing (Layer 3).

**Details:**
- VLAN interfaces (SVIs – Switched Virtual Interfaces) connect internal router logic.  
- Routing must be enabled manually on some switches.  
- Operates as L2 until routing is turned on.  
- Doesn’t fully replace a router — used for simpler internal routing.

---

## Data and Voice VLANs
**Old way:** Separate cable for phone and computer (PBX + switch).  
**Now:** Voice over IP (VoIP) — one Ethernet cable for both.

**Challenge:**  
Voice is latency-sensitive; data is not.  

**Solution:**  
Assign separate VLANs:
- Computer → Data VLAN (untagged access).  
- Phone → Voice VLAN (tagged with 802.1Q).  

Each interface supports both:
- Configured individually as Data VLAN + Voice VLAN.

---

# Interface Configuration

## Basic Settings
- **Speed:** 10 / 100 / 1,000 / 10,000 Mbps.  
- **Duplex:** Half / Full (must match both sides).  
- **IP management:**  
  - Layer 3 interfaces, VLAN interfaces, management ports.  
  - Includes IP, subnet mask, gateway, and DNS (optional).

---

## Link Aggregation
**What:** Combine multiple physical links into one logical interface.

- LAG (Link Aggregation Group) / Port Bonding.  
- **LACP (Link Aggregation Control Protocol):** adds automation and control.

---

## MTU (Maximum Transmission Unit)
**Purpose:** Maximum size of IP packet before fragmentation.  
- Fragmentation = bad (adds overhead, latency).  
- Path MTU discovery often unreliable (ICMP filtering).

---

## Jumbo Frames
**Definition:** Ethernet frames > 1,500 bytes payload (usually ~9,000 bytes).  
**Pros:** Higher efficiency, fewer packets.  
**Cons:** All network devices must support jumbo frames for compatibility.

---

# Spanning Tree Protocol (STP)

## Loop Protection
**Problem:**  
Connecting two switches twice creates an endless broadcast loop.  
No built-in counter at MAC layer → network collapse.

**Solution:**  
IEEE 802.1D **Spanning Tree Protocol (STP)** — prevents loops by blocking redundant links.

---

## STP Port States
1. **Blocking** – no forwarding (loop prevention).  
2. **Listening** – not forwarding, clearing MAC table.  
3. **Learning** – populating MAC table.  
4. **Forwarding** – full operational state.  
5. **Disabled** – port turned off by admin.

---

## Rapid Spanning Tree Protocol (RSTP)
**IEEE 802.1w** — modern version of STP.  
- Faster convergence: 6s vs 30–50s in STP.  
- Backwards-compatible with STP (802.1D).  
- Same logic, better performance.

---

## Read more
- planned.
