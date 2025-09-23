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

___________________________________________________________________________________________________________________________

## 🖥 Part I – Network Topologies

### 1. Bus Topology
The Bus topology connects multiple devices using a single central hub, simulating a shared communication medium. All PCs are connected to the hub, and data travels across the same backbone.

#### IPv4 Addressing Table
| Device | Interface | IPv4 Address  | Subnet Mask     | Default Gateway |
|--------|-----------|---------------|-----------------|----------------|
| PC0    | FastEthernet0 | 192.168.20.2 | 255.255.255.0 | 192.168.20.1 |
| PC1    | FastEthernet0 | 192.168.20.3 | 255.255.255.0 | 192.168.20.1 |
| PC2    | FastEthernet0 | 192.168.20.4 | 255.255.255.0 | 192.168.20.1 |
| PC3    | FastEthernet0 | 192.168.20.5 | 255.255.255.0 | 192.168.20.1 |

#### Screenshot
![Alt text](./images/Bus.jpeg)

#### Configuration Notes
- Used a hub to represent the shared bus.  
- All PCs configured in the same subnet.  
- Successful ping tests confirmed communication between devices.  

[Download the Cisco Packet Tracer topology - Bus](pkt-files/Bus.pkt)

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


#### Screenshot
![Alt text](./images/Star.jpeg)
#### ptk file
[Download the Cisco Packet Tracer topology - Star](pkt-files/Star.pkt)

#### Configuration Notes
- PCs connected to a central switch.  
- Each PC assigned IPv4 addresses in the same subnet.  
- Successful ping tests between PCs confirmed connectivity.

---

### 3. Mesh Topology
The Mesh topology connects every switch to every other switch, and each PC is connected to its dedicated switch. This setup ensures high redundancy and reliability. Even if one link fails, all PCs can still communicate through alternative paths.

#### IPv4 Addressing Table
| Device | Interface | IPv4 Address  | Subnet Mask     | Default Gateway |
|--------|-----------|---------------|-----------------|----------------|
| PC0    | FastEthernet0 | 192.168.30.2 | 255.255.255.0 | 192.168.30.1 |
| PC1    | FastEthernet0 | 192.168.30.3 | 255.255.255.0 | 192.168.30.1 |
| PC2    | FastEthernet0 | 192.168.30.4 | 255.255.255.0 | 192.168.30.1 |
| PC3    | FastEthernet0 | 192.168.30.5 | 255.255.255.0 | 192.168.30.1 |

#### Screenshot
![Alt text](./images/mesh.jpeg)

#### Configuration Notes
- Each PC connected to a dedicated switch.  
- All switches connected to every other switch to simulate full mesh connectivity.  
- Assigned IPv4 addresses within the same subnet.  
- Verified connectivity through ping tests between all PCs.  

[Download the Cisco Packet Tracer topology - Mesh](pkt-files/mesh.pkt)

---
### 4. Ring Topology
The Ring topology connects devices in a closed loop, where each device is connected to exactly two others, forming a circular pathway. Data travels in one or both directions around the ring.

#### IPv4 Addressing Table
| Device | Interface | IPv4 Address  | Subnet Mask     | Default Gateway |
|--------|-----------|---------------|-----------------|----------------|
| PC0    | FastEthernet0 | 192.168.40.2 | 255.255.255.0 | 192.168.40.1 |
| PC1    | FastEthernet0 | 192.168.40.3 | 255.255.255.0 | 192.168.40.1 |
| PC2    | FastEthernet0 | 192.168.40.4 | 255.255.255.0 | 192.168.40.1 |
| PC3    | FastEthernet0 | 192.168.40.5 | 255.255.255.0 | 192.168.40.1 |

#### Screenshot
![Alt text](./images/ring.jpeg)

#### Configuration Notes
- Each PC connected to a switch forming a circular ring.  
- Each switch connected to two other switches to complete the loop.  
- IPv4 addresses assigned in the same subnet.  
- Connectivity confirmed with successful ping tests around the ring.  

[Download the Cisco Packet Tracer topology - Ring](pkt-files/ring.pkt)

---

### 5. Extended Star Topology
The Extended Star topology is a hierarchical structure where a central switch connects to multiple peripheral switches, and each peripheral switch connects to several PCs. This design provides scalability and improved management compared to a simple star.

#### IPv4 Addressing Table
All devices are assigned IP addresses from the same subnet (192.168.50.0/24). This allows direct communication between all PCs without requiring a router.

| Device | Interface      | IPv4 Address   | Subnet Mask     | Default Gateway |
|--------|----------------|----------------|-----------------|----------------|
| PC0    | FastEthernet0  | 192.168.50.2   | 255.255.255.0   | 192.168.50.1   |
| PC1    | FastEthernet0  | 192.168.50.3   | 255.255.255.0   | 192.168.50.1   |
| PC2    | FastEthernet0  | 192.168.50.4   | 255.255.255.0   | 192.168.50.1   |
| PC3    | FastEthernet0  | 192.168.50.5   | 255.255.255.0   | 192.168.50.1   |
| PC4    | FastEthernet0  | 192.168.50.6   | 255.255.255.0   | 192.168.50.1   |
| PC5    | FastEthernet0  | 192.168.50.7   | 255.255.255.0   | 192.168.50.1   |
| PC6    | FastEthernet0  | 192.168.50.8   | 255.255.255.0   | 192.168.50.1   |
| PC7    | FastEthernet0  | 192.168.50.9   | 255.255.255.0   | 192.168.50.1   |
| PC8    | FastEthernet0  | 192.168.50.10  | 255.255.255.0   | 192.168.50.1   |
| PC9    | FastEthernet0  | 192.168.50.11  | 255.255.255.0   | 192.168.50.1   |
| PC10   | FastEthernet0  | 192.168.50.12  | 255.255.255.0   | 192.168.50.1   |
| PC11   | FastEthernet0  | 192.168.50.13  | 255.255.255.0   | 192.168.50.1   |

#### Screenshot
![Alt text](./images/exStar.jpeg) //external star

#### Configuration Notes
- 1 central switch connects to 4 peripheral switches.  
- Each peripheral switch connects to 3 PCs (total 12 PCs).  
- All PCs share the subnet 192.168.50.0/24 for simplicity.  
- Verified full connectivity with successful ping tests between PCs across all switches.  

[Download the Cisco Packet Tracer topology - Extended Star](pkt-files/exStar.pkt)

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

