# CMPG 325 Computer Networks Individual Project (2025)

## Faculty of Natural & Agricultural Science
**Department of Computer Science**

### Project Overview
This repository contains the implementation and documentation for the CMPG 325 Computer Networks semester - long project.  
The project demonstrates the design, configuration, and simulation of multiple network topologies using *Cisco Packet Tracer, with emphasis on IPv4 & IPv6 addressing, VLAN segmentation, server configuration, and network security.*

### Project Objectives
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

## 📝 Step 2 – First Topology: Bus
We’ll start simple with the **Bus Topology**.

🔧 **In Packet Tracer:**
- Devices: at least **3 PCs + 1 Switch/Hub (acting as the bus backbone)**.  
- Connect them linearly.  
- Assign IPv4 addresses (same subnet).  
- Test with `ping`.  

💻 **Example IPv4 Table (Bus Topology):**

| Device | Interface | IPv4 Address | Subnet Mask | Default Gateway |
|--------|-----------|--------------|-------------|----------------|
| PC0    | FastEthernet0 | 192.168.10.2 | 255.255.255.0 | 192.168.10.1 |
| PC1    | FastEthernet0 | 192.168.10.3 | 255.255.255.0 | 192.168.10.1 |
| PC2    | FastEthernet0 | 192.168.10.4 | 255.255.255.0 | 192.168.10.1 |
| Switch/Hub (Bus) | N/A | N/A | N/A | N/A |

⚡ **Testing:**  
- Use `ping 192.168.10.3` from PC0 → should succeed.  
- Repeat for all PCs.  

📸 **Documentation placeholder:**  
```markdown
### Bus Topology
The Bus topology connects all devices along a single communication line using a switch/hub as the backbone.  

#### IPv4 Addressing Table
| Device | Interface | IPv4 Address | Subnet Mask | Default Gateway |
|--------|-----------|--------------|-------------|----------------|
| PC0    | FastEthernet0 | 192.168.10.2 | 255.255.255.0 | 192.168.10.1 |
| PC1    | FastEthernet0 | 192.168.10.3 | 255.255.255.0 | 192.168.10.1 |
| PC2    | FastEthernet0 | 192.168.10.4 | 255.255.255.0 | 192.168.10.1 |

#### Screenshot
![Bus Topology Screenshot](images/bus_topology.png)

#### Configuration Notes
- All devices configured on the same subnet.
- Successful ping tests confirm communication between nodes.
````

