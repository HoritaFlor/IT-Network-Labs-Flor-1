# Proyecto de red Cisco Packet Tracer

# LAB3 – VLANs y segmentación de red

**Curso:** The Bits and Bytes of Computer Networking (Google)

**Autor:** Florencia Horita

**Fecha:** 12/11/2025

---

## Descripción

Este laboratorio demuestra cómo segmentar una red LAN utilizando VLANs (Virtual LANs) en switches Cisco 2960.
Se configuraron VLANs, se asignaron puertos a cada una y se estableció un trunk entre los switches para permitir la comunicación inter-VLAN a través del router.

---

## Objetivos

- Comprender el funcionamiento y propósito de las VLANs.

- Configurar VLANs en switches Cisco Catalyst 2960.

- Asignar puertos a VLANs específicas según el rol de cada equipo.

- Configurar un enlace troncal (trunk) entre switches.

- Verificar la conectividad dentro de cada VLAN y entre VLANs mediante un router.

## Topología de red

LAN con dos switches interconectados:

Switch 1 (Administración, Soporte) — Switch 2 (Ventas)

Ambos conectados mediante un enlace troncal (trunk) y un router para comunicación inter-VLAN.

---

## Configuraciones principales

- VLAN 10 → Administración

- VLAN 20 → Soporte

- VLAN 30 → Ventas

- Router Cisco 2911 → Configurado con subinterfaces para cada VLAN.

- Switches 2960 → VLANs creadas y puertos asignados a cada grupo de trabajo.

---

## Comandos usados

```bash
enable
configure terminal

# Crear VLANs
vlan 10
name Administracion
vlan 20
name Soporte
vlan 30
name Ventas
exit

# Asignar puertos a VLANs
interface fa0/1
switchport mode access
switchport access vlan 10
exit

interface fa0/2
switchport mode access
switchport access vlan 20
exit

# Configurar trunk entre switches
interface fa0/24
switchport mode trunk
exit

# Configurar subinterfaces en el router
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

## Resultados

• Comunicación exitosa dentro de cada VLAN.

• Conectividad inter-VLAN lograda mediante el router.

• Segmentación lógica de la red verificada mediante comandos y pruebas de ping.

• Proyecto guardado en formato .pkt y documentación .pdf.

---

## Archivos incluidos

LAB3_VLANS_SEGMENTACION_FLOR.pkt → Proyecto de Cisco Packet Tracer

LAB3_VLANS_SEGMENTACION_FLOR.pdf → Documentación técnica del laboratorio

---

## Observación

En este laboratorio se implementaron VLANs para separar lógicamente los departamentos de la red.

Se utilizó un enlace troncal (trunk) entre switches para permitir el paso de tráfico etiquetado de múltiples VLANs.

El router Cisco 2911 realizó el enrutamiento inter-VLAN a través de subinterfaces configuradas con encapsulation dot1Q.






