# IronGate: A Secure Multi-Branch Enterprise Network Architecture (IPv4 & IPv6)

## Project Overview
IronGate is an enterprise-grade **Blue Team network security simulation** designed and implemented using **Cisco Packet Tracer**.  
The project demonstrates a **secure, scalable, hierarchical enterprise network** connecting a **Headquarters (HQ)** with **four remote branches**, following best practices in routing, firewalling, VPN, Layer 2 security, and dual-stack IPv4/IPv6 deployment.

The architecture includes:
- 1 Headquarters (HQ)
- 4 Branches
- Centralized security at HQ
- Secure inter-branch connectivity
- Wired and Wireless infrastructure
- Defense-in-depth

The design focuses on **network defense and secure operations** rather than end-user services.

---

## Network Architecture
- HQ acts as the **central security and services hub**
- 1 Edge Router connected to an ISP
- 4 Branch Routers connected through the ISP
- 3 Branches operate in **Dual-Stack (IPv4 & IPv6)**
- Secure tunneling enables **IPv6 inter-branch communication**
- ASA Firewall deployed at HQ protecting a public **DMZ**

---

## Addressing & Subnetting
- IPv4 Base Network: `10.11.12.0/24`
  - Subnetted across:
    - HQ VLANs
    - Branch LANs
    - Management Networks
    - DMZ
    - Point to Point Networks
- IPv6 Base Network: `2000:12:34::/48`
  - Hierarchical IPv6 subnetting per site and VLAN
- DHCP used for IPv4 clients
- SLAAC + Stateless DHCP for IPv6 clients
- Clear subnet boundaries to demonstrate **proper enterprise subnetting design**

---

## Routing & Connectivity
- OSPFv2 for IPv4 routing
- Static routing for firewall and DMZ networks
- IPv6 Tunneling between branches to enable IPv6 communication
- Site-to-Site **IPSec VPN** securing traffic between HQ and branches

---

## Edge & WAN Security
- Edge Router performs:
  - Internet access control
  - VPN Gateway
- Zone-Based Policy Firewall (**ZPF**) implemented to control traffic between:
  - Inside
  - Outside
  - DMZ
- Stateful inspection applied based on security zones

---

## Firewall & DMZ Security
- **ASA 5506-X Firewall** deployed at HQ
- DMZ hosts publicly accessible services
- Controlled access from:
  - Internet → DMZ
  - Internal Network → DMZ
- No direct Internet access to internal networks

---

## Switching & Layer 2 Security
- Dedicated Management VLANs
- Dedicated Native VLAN for trunks
- Blackhole VLAN for unused ports
- All unused ports administratively shut down

### Implemented Layer 2 Security Features:
- Port Security
- DHCP Snooping
- Dynamic ARP Inspection (DAI)
- BPDU Guard
- 802.1X Authentication (where supported)

---

## Management & Control Plane Security
- SSH enabled on all network devices
- AAA using:
  - TACACS+
  - RADIUS
- Different authentication fallback priorities
- Role-Based Access Control (RBAC)
- Privilege levels and command authorization
- Secure device hardening:
  - Encrypted passwords
  - Banner warnings
  - Access restrictions

---

## Monitoring & Network Services
- Centralized Syslog Server
- NTP Server with authentication
- Log collection from routers, switches, and firewall

---

## Security Technologies Implemented
- Zone-Based Policy Firewall (ZPF)
- ASA Firewall with DMZ
- IPSec Site-to-Site VPN
- IPv4 & IPv6 ACLs
- NAT at the Edge Router
- Layer 2 attack mitigation
---

## Skills Demonstrated
- Enterprise network design (Hierarchical Model)
- Blue Team network defense
- Advanced subnetting (IPv4 & IPv6)
- Secure routing with OSPFv2 & OSPFv3
- Firewall & DMZ design
- IPSec VPN deployment
- Layer 2 security hardening
- Wireless security with WLC
- AAA & management plane security
- Dual-stack enterprise networking

---

## Tools & Technologies
- Cisco Packet Tracer
- Cisco IOS & ASA
- IPv4 / IPv6
- OSPFv2
- IPSec VPN
- ZPF
- NAT

---

## Project Type
**Enterprise Blue Team Network Security Lab**  
Designed for learning, demonstration, and portfolio showcasing.
