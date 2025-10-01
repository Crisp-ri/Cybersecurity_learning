---
title: "Ports and Protocols - TL;DR"
date: 2025-10-01
tags: [network, fundamentals, ports, protocols]
level: beginner
---

# Ports and Protocols

**What**: Standards that define how data is formatted and transmitted across a network. Ports identify specific services on a device, while protocols define the rules of communication.  
**Why it matters**: Without standardized ports and protocols, devices and applications wouldn’t understand each other, making the internet a noisy mess instead of (mostly) working.

---
## Common Protocols and Ports

- **HTTP (HyperText Transfer Protocol)** - Port **80**, used for web traffic (unencrypted).
- **HTTPS (HyperText Transfer Protocol Secure)** - Port **443**, encrypted web traffic via SSL/TLS.
- **FTP (File Transfer Protocol)** - Ports **20/21**, used to transfer files between client and server.
- **SFTP (SSH File Transfer Protocol)** - Port **22**, secure file transfer over SSH.
- **SSH (Secure Shell)** - Port **22**, secure remote login and command execution.
- **Telnet (Telecommunication Network)** - Port **23**, remote login without encryption (obsolete/insecure).
- **SMTP (Simple Mail Transfer Protocol)** - Port **25**, sending email.
- **POP3 (Post Office Protocol v3)** - Port **110**, receiving email (downloads mail to client).
- **IMAP (Internet Message Access Protocol)** - Port **143**, retrieving/managing email directly on the server.
- **DNS (Domain Name System)** - Port **53**, resolves domain names to IP addresses.
- **DHCP (Dynamic Host Configuration Protocol)** - Ports **67/68**, automatically assigns IP addresses.
- **TFTP (Trivial File Transfer Protocol)** - Port **69**, simple/unencrypted file transfers.
- **SNMP (Simple Network Management Protocol)** - Port **161**, used for managing devices on IP networks.
- **LDAP (Lightweight Directory Access Protocol)** - Port **389**, directory service protocol.
- **RDP (Remote Desktop Protocol)** - Port **3389**, remote graphical desktop access.

---
## Key Mechanisms

- **Port numbers** - logical endpoints for communication, ranging from 0-65535.  
  - **Well-known ports (0-1023)** - reserved for core protocols (HTTP, FTP, etc.).
  - **Registered ports (1024-49151)** - assigned to user processes/applications.
  - **Dynamic/Ephemeral ports (49152-65535)** - temporary ports chosen by the OS for connections.

- **TCP (Transmission Control Protocol)** - connection-oriented, reliable, error-checked delivery.
- **UDP (User Datagram Protocol)** - connectionless, faster but no guaranteed delivery.

---
## Read more
- planned.
