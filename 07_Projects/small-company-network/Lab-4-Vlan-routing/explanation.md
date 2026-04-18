# Lab 4: VLAN Configuration and Inter-VLAN Routing

## Objective
To design and implement a segmented network using VLANs and enable communication between them using router-on-a-stick.

---

## Network Topology
- 1 Router
- 1 Switch
- 3 VLANs (10, 20, 30)
- Multiple end devices (PCs)

---

## VLAN Design

| VLAN | Name  | Subnet          | Gateway        |
|------|------|-----------------|----------------|
| 10   | ADMIN | 192.168.10.0/24 | 192.168.10.1   |
| 20   | SALES | 192.168.20.0/24 | 192.168.20.1   |
| 30   | IT    | 192.168.30.0/24 | 192.168.30.1   |

---

## Key Configuration Steps

### 1. VLAN Creation on Switch
- VLANs 10, 20, 30 created and assigned to access ports

### 2. Trunk Configuration
- Switch port Fa0/24 configured as 802.1Q trunk to router

### 3. Router-on-a-Stick Setup
- Subinterfaces created:
  - Fa0/0.10 → VLAN 10
  - Fa0/0.20 → VLAN 20
  - Fa0/0.30 → VLAN 30

- Each subinterface assigned IP gateway

---

## Verification
- Ping tests confirmed successful communication within and between VLANs
- Router successfully routes traffic between all subnets

---

## Outcome
A fully functional segmented enterprise-style network with inter-VLAN routing.