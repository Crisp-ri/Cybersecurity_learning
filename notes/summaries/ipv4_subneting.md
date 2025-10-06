---
title: "IPv4 subnetting - TL;DR"
date: 2025-10-06
tags: [network, fundamentals, ipv4, binary, subnetting]
level: beginner
---

# Binary Math 
**What:** Binary math represents numbers using only two symbols: 0 and 1.  
**Why:** Computers use binary to process data, as hardware circuits recognize two states — on/off.

## Basics
- **Bit:** Smallest unit of data, either 0 or 1.  
- **Byte:** 8 bits (also called an *octet*).  
- **Binary-to-decimal conversion chart:**  
  | 128 | 64 | 32 | 16 | 8 | 4 | 2 | 1 |

## Binary → Decimal
1. `00000010` → 2  
2. `10000010` → 130  
3. `11111111` → 255  

## Decimal → Binary
Example: 154  
- Start from left:  
  128 ≤ 154 → 1  
  128 + 64 (192) > 154 → 0  
  Continue pattern → `10011010`  
- **Binary:** 10011010  
- **Decimal:** 128 + 16 + 8 + 2 = 154  

## Bit Ranges
| Bits | Combinations |
|------|---------------|
| 2 | 4 |
| 3 | 8 |
| 4 | 16 |
| 5 | 32 |
| 6 | 64 |
| 7 | 128 |
| 8 | 256 |

---

# IPv4 Addressing 
**What:** IPv4 assigns unique numerical labels to devices in a network.  
**Why:** Enables identification and communication between devices.

## Basic Components
- **IP Address:** e.g., `192.168.1.165` — unique per device.  
- **Subnet Mask:** e.g., `255.255.255.0` — defines the subnet boundary.  
- **Default Gateway:** e.g., `192.168.1.1` — router that connects to external networks.

## Special IPv4 Addresses
- **Loopback:** 127.0.0.1–127.255.255.254 (self-reference for testing).  
- **Reserved:** 240.0.0.1–254.255.255.254 (future use, testing).  
- **Virtual (VIP):** Logical addresses, not tied to physical adapters.

## IPv4 Format
- Layer 3 OSI address.  
- Example: `192.168.1.131` → `11000000 10101000 00000001 10000011` (4 bytes).

## DHCP (Dynamic Host Configuration Protocol)
**What:** Automatically assigns IP configurations.  
**Why:** Simplifies setup by avoiding manual configuration.

## APIPA (Automatic Private IP Addressing)
- **Range:** 169.254.0.1–169.254.255.254  
- **Purpose:** Allows local communication when DHCP fails.  
- Uses ARP to ensure address uniqueness.

## Private IP Ranges (RFC 1918)
| Range | Class | Use |
|--------|--------|-----|
| 10.0.0.0–10.255.255.255 | A | Large networks |
| 172.16.0.0–172.31.255.255 | B | Medium networks |
| 192.168.0.0–192.168.255.255 | C | Small networks |

Private IPs are not Internet-routable; use NAT for external communication.

---

# Classful Subnetting 
**What:** Original IP classification by network size (A, B, C).  
**Why:** Simplified early routing; now replaced by CIDR but still referenced.

| Class | Network Bits | Host Bits |
|--------|---------------|-----------|
| A | 8 | 24 |
| B | 16 | 16 |
| C | 24 | 8 |

## Subnet Construction
- **Network address:** All host bits = 0.  
- **First usable:** Network + 1.  
- **Broadcast address:** All host bits = 1.  
- **Last usable:** Broadcast − 1.

### Example
IP: `10.74.222.11` (Class A, mask 255.0.0.0)  
| Type | Address |
|------|----------|
| Network | 10.0.0.0 |
| First Host | 10.0.0.1 |
| Broadcast | 10.255.255.255 |
| Last Host | 10.255.255.254 |

---

# IPv4 Subnet Masks 
**What:** Define which part of an IP is network vs. host.  
**Why:** Helps determine routing and subnet membership.

## Classless (CIDR)
- Introduced in 1993.  
- Removes rigid class boundaries.  
- Format: `192.168.1.44/24`  
- `/24` → 24 bits for network, 8 for host.

## Mask Rules
- Contiguous 1s for network portion.  
- Zeros for host portion.  
Example: `11111111.11111111.11111111.00000000` = `255.255.255.0`.

---

# Calculating Subnets & Hosts
**What:** Determines how many networks and hosts can exist.  
**Why:** Used for efficient IP planning.

## VLSM (Variable Length Subnet Mask)
Allows different masks within one classful network for flexibility.  
Example:  
- Base: `10.0.0.0/8`  
- Subnets: `10.0.1.0/24`, `10.0.8.0/26`

### Formula
- **Subnets:** 2^(subnet bits)  
- **Hosts per subnet:** 2^(host bits) − 2

---

# Magic Number Subnetting 
**What:** Shortcut for subnet calculations.  
**Why:** Faster method for finding subnet ranges and broadcast addresses.

### Example
IP: `165.245.77.14`, Mask: `255.255.240.0`  
1. Interesting octet: 240 → 256 − 240 = **16** (magic number).  
2. Subnet ID: `165.245.64.0`  
3. Broadcast: `165.245.79.255`  
4. First Host: `165.245.64.1`  
5. Last Host: `165.245.79.254`

---
## Read more
- planned.
