# Cisco Packet Tracer Network Project

# LAB2 – LAN Interconnection

**Course:** The Bits and Bytes of Computer Networking (Google)

**Author:** Florencia Horita

**Date:** 11/01/2025

---

## Description

This lab demonstrates how to interconnect two LAN networks using a Cisco 2911 router, enabling communication between different IP subnets.
The router interfaces, switches, and PCs were configured, and connectivity was verified using the ping command.

---

## Objectives

- Understand how a router enables communication between different IP subnets.

- Configure the interfaces of the Cisco 2911 router.

- Assign IPs, subnet masks, and gateways to the PCs in both LANs.

- Verify connectivity using ping tests.

---

## Network Topology
LAN1 --- Switch 2960 --- Router 2911 --- Switch 2960 --- LAN2

---

## Main Configurations

- **LAN1** → Network: 192.168.1.0/24

- **LAN2** → Network: 192.168.2.0/24

- **Cisco 2911 Router** → Interfaces Gig0/0 and Gig0/2 configured and active

- **Catalyst 2960 Switches** → Connect the PCs within each LAN

---

Commands Used
```enable
configure terminal
interface gig0/0
ip address 192.168.1.1 255.255.255.0
no shutdown
interface gig0/2
ip address 192.168.2.1 255.255.255.0
no shutdown
end
show ip interface brief
```
---

## Results
• Successful communication between both networks using ping.

• Router interface table verified.

• Project saved in .pkt format with technical documentation in .pdf.

---

## Included Files

LAB2_INTERCONEXION_DE_LANS_FLOR.pkt → Cisco Packet Tracer project file

LAB2_INTERCONEXION_DE_LANS_FLOR.pdf → Technical documentation of the lab
