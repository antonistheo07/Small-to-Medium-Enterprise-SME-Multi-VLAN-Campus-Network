# Small-to-Medium Enterprise (SME) Multi-VLAN Campus Network

![Topology Overview](docs/network-topology.png)

A fully segmented, secure campus Local Area Network (LAN) deployment for a small-to-medium enterprise featuring department-level isolation, centralized Layer 3 routing, dynamic addressing, edge port security, and dynamic NAT/PAT for outbound internet connectivity.

---

## 📑 Project Overview

* **Objective:** Design, configure, and secure a multi-department campus network ensuring isolation between sensitive departments (HR, Guest) while maintaining controlled management access for IT administrators.
* **Target Audience/Scale:** SME environment (~150-300 hosts across 4 operational domains).
* **Implementation Platform:** Cisco IOS (Cisco Packet Tracer).

---

## 🌐 Network Topology & Subnetting Plan

| Department | VLAN ID | Network Address | Subnet Mask | Default Gateway | Usable Hosts |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **IT Management** | `VLAN 10` | `10.10.10.0/24` | `255.255.255.0` | `10.10.10.1` | 254 |
| **Sales** | `VLAN 20` | `10.10.20.0/24` | `255.255.255.0` | `10.10.20.1` | 254 |
| **HR** | `VLAN 30` | `10.10.30.0/24` | `255.255.255.0` | `10.10.30.1` | 254 |
| **Guest Wi-Fi** | `VLAN 40` | `172.16.40.0/24` | `255.255.255.0` | `172.16.40.1` | 254 |
| **Server/DHCP Farm**| `VLAN 99` | `10.10.99.0/24` | `255.255.255.0` | `10.10.99.1` | 254 |
| **ISP Link (WAN)** | N/A | `203.0.113.0/30` | `255.255.255.252` | `203.0.113.2` | 2 |

