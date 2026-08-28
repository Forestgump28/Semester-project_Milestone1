# Semester-project_Milestone1
# CMPG325 Network Infrastructure Project
## Ratlou Local Municipality Offices (Setlagole)

**Student Name:** MZOBE, BAYA  
**Student Number:** 44027516  
**Module Code:** CMPG325  
**Submission Date:** 28 August 2026 (Milestone 1)  

---

## 📌 Executive Project Overview
This repository contains the local area network (LAN) design, VLSM addressing scheme, Packet Tracer simulation, and configuration evidence for the **Ratlou Local Municipality Offices** in Setlagole. 

The network architecture delivers segmented, secure, and scalable connectivity for administrative staff, public Wi-Fi users, and secondary floor infrastructure expansions.

> 📄 **Full Technical Report:** All detailed network design rationales, complete CLI configuration dumps, testing evidence, and architectural descriptions are fully documented in the submitted project PDF document (`CMPG325_Milestone1_44027516.pdf`).

---

## 📐 Network Architecture & Addressing Plan

* **Root Addressing Block:** `192.168.44.0/24`
* **Routing Strategy:** Router-on-a-Stick (802.1Q Inter-VLAN Routing on `R1-Ratlou`)
* **Core Switch:** `SW1-Core` using IEEE 802.1Q trunk links with aligned Native VLAN 99.

### Subnet Allocation Table (VLSM)

| Subnet / Function | VLAN ID | Network Address | Subnet Mask | Usable Host Range | Default Gateway |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Admin & Staff** | VLAN 10 | `192.168.44.0/26` | `255.255.255.192` | `192.168.44.1 – 192.168.44.62` | `192.168.44.1` |
| **Public Wi-Fi Zone** | VLAN 20 | `192.168.44.64/27` | `255.255.255.224` | `192.168.44.65 – 192.168.44.94` | `192.168.44.65` |
| **CR2 Expansion Floor** | VLAN 30 | `192.168.44.96/27` | `255.255.255.224` | `192.168.44.97 – 192.168.44.126` | `192.168.44.97` |
| **Management Subnet** | VLAN 99 | `192.168.44.128/28` | `255.255.255.240` | `192.168.44.129 – 192.168.44.142` | `192.168.44.129` |

---

## 🛠️ Repository Contents

```text
├── CMPG325_Milestone1_44027516.pkt   # Active Cisco Packet Tracer simulation file
├── CMPG325_Milestone1_44027516.pdf   # Complete technical report and documentation
└── README.md                          # Repository overview and summary
