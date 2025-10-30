# LAB1 - Basic LAN Network (Cisco Packet Tracer)

**Course:** The Bits and Bytes of Computer Networking (Google)  

**Author:** Florencia Horita

**Date:** 30/10/2025 

---

## Description  
This lab demonstrates the configuration of a simple LAN network using a Cisco Catalyst 2960 switch and three computers.  
It includes IP assignment, interface descriptions, hostname configuration, and verification of connectivity between devices through basic Cisco IOS commands.  

---

## Objectives  
- Understand how a Local Area Network (LAN) works.  
- Configure a Cisco 2960 (IOS 15.0) switch with hostname and interfaces.  
- Assign IPs to PCs and test connectivity between them.  
- Observe MAC addresses and the switch MAC table.  

---

## Topology  
[PC-User1] ---\

[PC-User2] ----> [Switch 2960]

[PC-User3] ---/


---

## Main Configurations  
- **IPs:** 192.168.1.2 / 192.168.1.3 / 192.168.1.4  
- **Subnet Mask:** 255.255.255.0  
- **Gateway:** Not configured (internal network without router)  
- **Switch Hostname:** SW-LAB1  
- **Configured Interfaces:** FastEthernet 0/1, 0/2, 0/3  

---

## Commands Used  
```enable
configure terminal
hostname SW-LAB1
interface fa0/1
description Connection to PC-User1 (192.168.1.2)
interface fa0/2
description Connection to PC-User2 (192.168.1.3)
interface fa0/3
description Connection to PC-User3 (192.168.1.4)
end
show running-config
show mac address-table
copy running-config startup-config
```

---

## Results  
- Successful communication between all PCs using **ping**.  
- MAC address table correctly generated.  
- Project verified and saved in both Packet Tracer (.pkt) and PDF (.pdf) formats.  

---

## Included Files  
- `LAB1_LAN_BASICA_ISA.pkt` → Packet Tracer project file.  
- `LAB1_LAN_BASICA_ISA_EN.pdf` → Technical documentation (bilingual).  



