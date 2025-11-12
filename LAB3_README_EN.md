# Cisco Packet Tracer Network Project  
# LAB3 – VLANs and Network Segmentation  

**Course:** The Bits and Bytes of Computer Networking (Google)  

**Author:** Florencia Horita 

**Date:** 11/12/2025  

---

## Description  

This lab demonstrates how to segment a LAN using VLANs (Virtual LANs) on Cisco Catalyst 2960 switches.  
VLANs were created, ports were assigned to each one, and a trunk link was established between switches to enable inter-VLAN communication through the router.  

---

## Objectives  

- Understand the operation and purpose of VLANs.  

- Configure VLANs on Cisco Catalyst 2960 switches.  

- Assign ports to specific VLANs according to each device’s role.  

- Configure a trunk link between switches.  

- Verify connectivity within each VLAN and between VLANs through the router.  

---

## Network Topology  

LAN with two interconnected switches:  

Switch 1 (Administration, Support) — Switch 2 (Sales)  

Both connected through a trunk link and a router for inter-VLAN communication.  

---

## Main Configurations  

- VLAN 10 → Administration  
- VLAN 20 → Support  
- VLAN 30 → Sales  

- **Router Cisco 2911:** Configured with subinterfaces for each VLAN.  
- **Switches Cisco 2960:** VLANs created and ports assigned to each workgroup.  

---

## Commands Used  

```bash
enable
configure terminal

# Create VLANs
vlan 10
name Administration
vlan 20
name Support
vlan 30
name Sales
exit

# Assign ports to VLANs
interface fa0/1
switchport mode access
switchport access vlan 10
exit

interface fa0/2
switchport mode access
switchport access vlan 20
exit

# Configure trunk between switches
interface fa0/24
switchport mode trunk
exit

# Configure router subinterfaces
interface gig0/0.10
encapsulation dot1Q 10
ip address 192.168.10.1 255.255.255.0

interface gig0/0.20
encapsulation dot1Q 20
ip address 192.168.20.1 255.255.255.0

interface gig0/0.30
encapsulation dot1Q 30
ip address 192.168.30.1 255.255.255.0
```
---

## Results

• Successful communication within each VLAN.

• Inter-VLAN connectivity achieved through the router.

• Logical segmentation verified via commands and ping tests.

• Project saved in .pkt format and documented in .pdf.

---

## Files Included

LAB3_VLANS_FLOR.pkt → Cisco Packet Tracer project file

LAB3_VLANS_FLOR.pdf → Technical documentation of the lab

---

## Observation

In this lab, VLANs were implemented to logically separate departments within the network.

A trunk link between switches was used to allow tagged traffic from multiple VLANs to pass through.

The Cisco 2911 router performed inter-VLAN routing using subinterfaces configured with encapsulation dot1Q.

