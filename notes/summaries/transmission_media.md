---
title: "Transmission media - TL;DR"
date: 2025-10-02
tags: [network, fundamentals, transmission media, wireless, ethernet, fiber, copper]
level: beginner
---

# Network Media and Wireless

**What**: Physical and wireless technologies that carry network traffic.  
**Why it matters**: Every attack path depends on the medium - wireless signals, copper, or fiber. Weaknesses here can mean interception, downtime, or full compromise.

---

## Wireless Standards

- **802.11 (Wi-Fi)** - IEEE wireless LAN standard. Marketed as Wi-Fi 4/5/6/6E etc. (e.g., 802.11ax = Wi-Fi 6).  
- **4G / LTE (Long Term Evolution)** - "4G" mobile networking, supports up to ~150 Mbit/s (LTE-A ~300 Mbit/s).  
- **5G** - Next-gen cellular. Launched 2020, speeds from 100 Mbit/s up to 10 Gbit/s. Key enabler for IoT.  
- **Satellite networking** - Non-terrestrial link. Useful for remote areas. High cost and latency (~250 ms). Starlink aims for 20-40 ms.

---

## Ethernet Standards

- **Ethernet** - The most widely used LAN tech. Supports twisted pair copper and fiber.  
- **Standard notation** - Example: `1000BASE-T`  
  - **1000** - speed in Mbit/s  
  - **BASE** - baseband transmission  
  - **T/F/SX** - medium: twisted pair, fiber, short-wave fiber, etc.  

---

## Optical Fiber

- **Fiber communication** - Data sent as light. Immune to RF interference, secure against casual tapping.  
- **Multimode fiber** - Short range, up to 2 km. Cheap LEDs.  
- **Singlemode fiber** - Long range, up to 100 km. Expensive laser.

---

## Copper Cabling

- **Twisted pair** - Balanced wiring (Transmit+, Transmit-). Twists cancel interference. Defined by IEEE 802.3 categories (Cat5e, Cat6, etc.).  
- **Coaxial cable (RG-6)** - Used in TV and cable Internet.  
- **Twinax** - Short-range (≤5 m), low latency, common in 10 Gbit Ethernet.  
- **Plenum vs non-plenum** - Fire-rated jackets for cables in air ducts and risers.

---

## Network Transceivers

- **Transceiver** - Transmitter + receiver in one module. Modular design (Ethernet, Fibre Channel, etc.).  
- **SFP (Small Form-factor Pluggable)** - 1 Gbit/s fiber or RJ45.  
- **SFP+** - Same size, supports 10-16 Gbit/s.  
- **QSFP / QSFP+** - 4-channel SFP modules (up to 40 Gbit/s).

---

## Fiber Connectors

- **SC (Subscriber Connector)** - Square push-on connector, common in data centers.  
- **LC (Local Connector)** - Compact, clip-style, very common.  
- **ST (Straight Tip)** - Bayonet "stick-and-twist."  
- **MPO (Multi-fiber Push On)** - 12 fibers in one connector, used for high-density links.

---

## Copper Connectors

- **RJ11** - 6P2C, used for telephony/DSL.  
- **RJ45** - 8P8C, standard Ethernet connector.  
- **F-connector** - Threaded coaxial connector, used in TV and DOCSIS cable modems.  
- **BNC (Bayonet Neill-Concelman)** - Coax/twinax connector, twist-lock. Found in video, DS3 WAN, lab gear.

---

## Read more

- IEEE 802 standards documentation  
- Wi-Fi Alliance
