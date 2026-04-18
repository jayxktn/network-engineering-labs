# Small Company Network – VLAN Segmentation & Inter-VLAN Routing

## Overview
This project simulates a small enterprise network using Cisco Packet Tracer. It demonstrates VLAN segmentation, trunking, and inter-VLAN routing using a router-on-a-stick architecture.

The goal was to design, implement, and troubleshoot a functional multi-VLAN network with end-to-end connectivity between departments.

---

## Network Architecture

- **Device Types:** 1 Router, 1 Switch, Multiple PCs
- **Design:** Router-on-a-Stick
- **Switching:** VLAN-based segmentation
- **Routing:** Inter-VLAN routing via subinterfaces

---

## VLAN Design

| VLAN | Department | Subnet            | Gateway          |
|------|------------|------------------|------------------|
| 10   | ADMIN      | 192.168.10.0/24  | 192.168.10.1     |
| 20   | SALES      | 192.168.20.0/24  | 192.168.20.1     |
| 30   | IT         | 192.168.30.0/24  | 192.168.30.1     |

---

## Key Technologies Used

- VLAN Configuration (Layer 2 segmentation)
- 802.1Q Trunking
- Router-on-a-Stick Inter-VLAN Routing
- IPv4 Subnetting
- CLI-based network configuration

---

## Verification

- Successful intra-VLAN communication
- Successful inter-VLAN routing via router
- End-to-end connectivity validated using ICMP (ping tests)

---

## Challenges & Debugging Experience

During implementation, multiple issues were encountered including:
- Switch port state issues (down/up inconsistencies)
- VLAN miscommunication during early testing
- Packet loss during inter-VLAN testing
- ARP resolution instability during initial convergence

These were resolved through systematic troubleshooting using:
- `show vlan brief`
- `show interfaces trunk`
- `show ip interface brief`
- PC-level IP verification
- ARP table clearing and retesting

---

## Outcome

A fully functional segmented enterprise-style network was successfully implemented and verified with stable inter-VLAN communication.