# CMPG 325 Computer Networks Individual Project (2025)

## Faculty of Natural & Agricultural Science
**Department of Computer Science**

---

## 📌 Project Overview
This repository contains the implementation and documentation for the CMPG 325 Computer Networks semester-long project.  
The project demonstrates the design, configuration, and simulation of multiple network topologies using Cisco Packet Tracer, with emphasis on IPv4 & IPv6 addressing, VLAN segmentation, server configuration, and network security.

---

## 🎯 Project Objectives
1. **Part I – Network Topologies Design & Simulation (60%)**  
   - Implement Bus, Mesh, Star, Ring, and Extended Star topologies.  
   - Design a Hybrid topology integrating elements of the above.  
   - Configure IPv4/IPv6 addressing, VLAN segmentation, servers (HTTP/DNS/DHCP), and basic security.  
   - Document the process with IP tables, screenshots, and configuration notes.  

2. **Part II – Network Feature Configuration (20%)**  
   - Configure Port-based VLANs with trunking (802.1Q).  

3. **Part III – Video Demonstration (20%)**  
   - Record a 15–30 minute demonstration video explaining the designs, configurations, and testing results.  

---

## 🖥 Part I – Network Topologies

### 1. Bus Topology
*(To be completed after Star)*

---

### 2. Star Topology
The Star topology connects all devices to a central switch. Each PC has its own dedicated link to the switch, making it reliable and easy to manage.

#### IPv4 Addressing Table
| Device | Interface | IPv4 Address  | Subnet Mask     | Default Gateway |
|--------|-----------|---------------|-----------------|----------------|
| PC0    | FastEthernet0 | 192.168.10.2 | 255.255.255.0 | 192.168.10.1 |
| PC1    | FastEthernet0 | 192.168.10.3 | 255.255.255.0 | 192.168.10.1 |
| PC2    | FastEthernet0 | 192.168.10.4 | 255.255.255.0 | 192.168.10.1 |
| PC3    | FastEthernet0 | 192.168.10.5 | 255.255.255.0 | 192.168.10.1 |

#### ptk file
![Alt text](./pkt-files/Star.pkt

#### Screenshot
![Alt text](./images/Star.jpeg)

________________________________________________________________________________________________________________________
#### Configuration Notes
- PCs connected to a central switch.  
- Each PC assigned IPv4 addresses in the same subnet.  
- Successful ping tests between PCs confirmed connectivity.

---

## 🖧 Part II – VLAN Configuration (802.1Q)
*(To be completed later)*

---

## 🎥 Part III – Video Demonstration
*(To be completed after documentation and configuration are done)*

---

## ✅ Conclusion
This project demonstrates the design and configuration of multiple network topologies in Cisco Packet Tracer, the implementation of VLANs, and the documentation of results in line with the CMPG 325 rubric.

---

