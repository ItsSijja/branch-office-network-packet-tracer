# Branch Office Network Design & Simulation (Cisco Packet Tracer)

Design and simulation of a standalone branch office network for a growing business scenario, built in Cisco Packet Tracer with a single Cisco 2911 router and a Cisco 2960 switch. It supports three departments (Admin, Finance and Customer Service) with both wired and wireless connectivity.

## Network Topology

![Network Topology](Network%20topology%20diagram.png)

## Project Scenario & Objectives

- Design a branch network using a **Cisco 2911 Router** and **Cisco 2960 Switch**
- Separate three departments into isolated VLANs
- Provide wired and wireless access for each department
- Automate IP address allocation with DHCP
- Enable routed communication between all departments

## IP Addressing & VLAN Plan

The assigned base network **192.168.1.0/24** was divided into three **/26** subnets.

| Department       | VLAN    | Subnet            |
|------------------|---------|-------------------|
| Admin            | VLAN 10 | 192.168.1.0/26    |
| Finance          | VLAN 20 | 192.168.1.64/26   |
| Customer Service | VLAN 30 | 192.168.1.128/26  |

## Key Implementations

- **IP Addressing & Subnetting:** Partitioned 192.168.1.0/24 into dedicated /26 subnets.
- **VLAN Segmentation:** Configured 802.1Q VLANs on the switch to isolate departmental broadcast domains.
- **Inter-VLAN Routing:** Implemented Router-on-a-Stick (ROAS) using router sub-interfaces.
- **DHCP:** Configured centralized DHCP pools and default gateways on the router for all wired and wireless clients.
- **Wireless LAN (WLAN):** Integrated a dedicated access point for each department, mapped to its VLAN.

## Verification & Testing

- Verified dynamic IP leasing on PCs, laptops, smartphones and network printers
- Validated end-to-end ICMP reachability (ping) and default gateway connectivity across all inter-VLAN and wireless paths
- Verified 802.1Q trunking and sub-interface states using Cisco IOS CLI

**Commands used:** `show vlan brief`, `show interfaces trunk`, `show ip interface brief`, `show ip dhcp pool`

### DHCP Verification
![DHCP Verification](DHCP%20Verification.png)

### Inter-VLAN Ping Verification
![Inter-VLAN Ping Verification](Inter-VLAN%20Ping%20Verification.png)

### Router Verification
![Router Verification CLI](Router%20Verification%20CLI.png)

### Switch Verification
![Switch Verification CLI](Switch%20Verification%20CLI.png)

## Technologies Used

Cisco Packet Tracer, Cisco IOS CLI, VLANs (802.1Q), Router-on-a-Stick, DHCP, IPv4 Subnetting, WLAN

## How to Open the Project

1. Install [Cisco Packet Tracer](https://www.netacad.com/)
2. Download `P01.pkt` from this repository
3. Open it in Packet Tracer and explore the devices and configurations

## Author

**Sithijaya Sayuranga**
[GitHub](https://github.com/ItsSijja)
