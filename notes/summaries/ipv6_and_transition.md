---
title: "IPv6 Addressing - TL;DR"
date: 2025-10-08
tags: [network, ipv6, addressing]
level: intermediate
---

# IPv6 Addressing

**What:** IPv6 is the next generation Internet Protocol designed to replace IPv4, offering a massive 128-bit address space and modern mechanisms for configuration and communication.  
**Why it matters:** IPv4 address exhaustion, compatibility issues, and scalability limits make IPv6 essential for continued global Internet growth.

---

## IPv4 Address Exhaustion

There are over 20 billion devices connected to the Internet, but IPv4 only supports about 4.29 billion addresses.  
The IPv4 space is exhausted — no new unique addresses are available.  
IPv4 with NAT is only a temporary workaround and can cause issues with certain protocols.  
IPv6 solves this with a much larger address space and future growth capacity.

---

## IPv6 Addresses

Internet Protocol version 6 uses 128-bit addresses — allowing 340,282,366,920,938,463,374,607,431,768,211,456 (340 undecillion) possible addresses.  
Every grain of sand on Earth could have about 45 quintillion unique IPv6 addresses.

---

## IPv6 Address Compression

Groups of zeros can be shortened with a double colon (`::`) — only once per address.  
Leading zeros in each group are optional.  

Example:  
`2600:DDDD:1111:0001:0000:0000:0000:0001` → `2600:DDDD:1111:1::1`

---

## Communicating Between IPv4 and IPv6

Not all devices can use IPv6 (e.g., legacy systems).  
To bridge the gap, several mechanisms exist:  
- Tunnel — Encapsulate one protocol within another.  
- Dual-stack — Run both IPv4 and IPv6 simultaneously.  
- Translate — Convert between protocols.  

These are short-term solutions; the long-term goal is full IPv6 migration.

---

## Tunneling IPv6

Used as a temporary migration method.  

**6to4 addressing:**  
- Sends IPv6 over existing IPv4 networks.  
- Creates IPv6 addresses based on IPv4.  
- Requires relay routers and does not support NAT.  
- Deprecated in Windows.

**4in6 tunneling:**  
- Encapsulates IPv4 traffic within IPv6 networks.

---

## Dual-Stack Routing

Run IPv4 and IPv6 together.  
Each interface gets both IPv4 and IPv6 addresses.  

**IPv4:**  
- Uses IPv4 addresses and routing protocols.  
- Maintains an IPv4 routing table.

**IPv6:**  
- Uses IPv6 addresses and routing protocols.  
- Maintains a separate IPv6 routing table.

---

## Translating Between IPv4 and IPv6

**NAT64** translates traffic between IPv4 and IPv6 seamlessly for end users.  
Requires a NAT64-capable router since IPv6 is not backward compatible with IPv4.  
Works with **DNS64** to translate DNS requests accordingly.

---

# IPv6 and SLAAC

## Automatic IP Addressing in IPv6

**DHCPv6:**  
- Similar to IPv4 DHCP but requires redundant servers and active management.  

**Stateless Addressing (SLAAC):**  
- No dedicated DHCP server or lease tracking.  
- Automatically assigns addresses without maintaining state.

---

## NDP (Neighbor Discovery Protocol)

Replaces ARP and broadcast communication with ICMPv6 multicast.  
Functions include:  
- **Neighbor MAC Discovery** — Finds MAC addresses.  
- **SLAAC** — Automatically configures IP addresses.  
- **DAD (Duplicate Address Detection)** — Ensures uniqueness.  
- **Router Discovery** — Uses Router Solicitation (RS) and Router Advertisement (RA).

---

## Finding Routers

Routers send **unsolicited RA** (Router Advertisement) messages from multicast address `ff02::1`.  
RA includes IPv6 address info, prefix, prefix length, DNS servers, and more.  
NDP provides ICMPv6-based discovery of network routers.

---

## SLAAC Process

1. Use NDP (RS/RA) to determine the network prefix.  
2. Combine it with a modified **EUI-64** (or randomized) host portion to form a complete address.  
3. Run **DAD (Duplicate Address Detection)** to ensure address uniqueness before use.

---
## Read more
- planned.
