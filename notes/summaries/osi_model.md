---
title: "OSI model - TL;DR"
date: 2025-09-22
tags: [network, osi, fundamentals]
level: begginer
---

# OSI Model - TL;DR

**What**: The OSI (Open System Interconnection) model is a 7-layer framework for understanding how different networking protocols interact.
**Why it matters**: Help standardize networking concepts and troubleshooting.


---
## Layers (from top to bottom)

1. **Application** - User interaction (HTTP, SMTP, FTP, POP3).
2. **Presentation** - Data translation, encryption (TLS, SSL).
3. **Session** - Manage sessions, connections.
4. **Transport** - Reliability, flow control (TCP, UDP).
5. **Network** - Routing, addressing (IP).
6. **Data Link** - Frames, MAC addresses (Ethernet).
7. **Physical** - Hardware, cabels, bits.

---

## Quick checks / commands
- `ping <host>` - test Network layer (IP).
- `traceroute <host>` - shows Network layer routing.
- `netstart -an` - active connections (Transport layer).
- Wireshark - analyze packets across multiple layers.

---

## Mnemonics
- Top to bottom: *All People Seem To Need Data Processing"
- Bottom to top: "Please Do Not Throw Sausage Pizza Away"

---

## Read more
- OSI model is considered foundational; no deep dive required.
