# Multi-Site VLAN Network — Cisco Packet Tracer

**Author:** Jorge Antonio Nava  
**Date:** May 2026  
**Tools:** Cisco Packet Tracer · 2× Cisco 2901 · Cisco 2960 · Cisco 3560 

---

## Overview

A dual-site enterprise network simulation demonstrating VLAN segmentation, inter-VLAN routing, WAN connectivity, and ACL-based traffic control.

---

## Network topology

| Device | Role |
|---|---|
| Router0 (2901) | Site A gateway — router-on-a-stick for VLAN10 & VLAN20 |
| Router1 (2901) | Site B gateway — WAN uplink + subinterface routing |
| Switch0 (2960) | Site A Layer 2 switch — trunk to Router0 |
| Multilayer Switch (3560) | Site B Layer 3 switch — SVI routing |

---

## IP addressing

| Location | VLAN | Subnet | Gateway |
|---|---|---|---|
| Router0 — HR | VLAN10 | 192.168.10.0/24 | 192.168.10.1 |
| Router0 — Accounting | VLAN20 | 192.168.20.0/24 | 192.168.20.1 |
| Router1 — HR | VLAN10 | 192.168.30.0/24 | 192.168.30.1 |
| Router1 — Accounting | VLAN20 | 192.168.40.0/24 | 192.168.40.1 |
| WAN link | — | 10.0.0.0/30 | R0: 10.0.0.1 · R1: 10.0.0.2 |

---

## ACL traffic policy

| Source | Destination | Result |
|---|---|---|
| HR (any site) | HR (any site) | Allowed |
| Accounting (any site) | Accounting (any site) | Allowed |
| HR | Accounting | Blocked |
| Accounting | HR | Blocked |

---

## Key concepts demonstrated

- Router-on-a-Stick (802.1Q subinterfaces)
- Layer 3 SVI routing on Cisco 3560
- Extended named ACLs applied inbound on subinterfaces
- Static routing with specific and default routes
- Point-to-point /30 WAN link between routers
- Trunk port configuration (dot1Q encapsulation)
- Systematic troubleshooting using show ip route, show ip interface brief, ping
