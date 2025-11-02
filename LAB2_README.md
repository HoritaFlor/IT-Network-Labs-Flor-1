# Proyecto de red Cisco Packet Tracer

# LAB2 – Interconexión de LANs

**Curso:** The Bits and Bytes of Computer Networking (Google)  

**Autor:** Florencia Horita

**Fecha:** 01/11/2025  

---

## Descripción

Este laboratorio muestra cómo interconectar dos redes LAN mediante un router Cisco 2911, permitiendo la comunicación entre diferentes subredes IP.
Se configuraron las interfaces del router, los switches y las PCs, comprobando conectividad mediante el comando ping.

---

## Objetivos

- Comprender cómo un router permite la comunicación entre subredes IP.

- Configurar las interfaces del router Cisco 2911.

- Asignar IPs, máscaras y gateways a las PCs de ambas LANs.

- Verificar conectividad mediante pruebas de ping.

---

## Topología de red

LAN1 --- Switch 2960 --- Router 2911 --- Switch 2960 --- LAN2

---

## Configuraciones principales

- LAN1 → Red: 192.168.1.0/24

- LAN2 → Red: 192.168.2.0/24

- Router Cisco 2911 → Interfaces Gig0/0 y Gig0/2 activas

- Switches Catalyst 2960 → Conectan las PCs de cada LAN

---

## Comandos usados

```bash
enable
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

## Resultados

• Comunicación exitosa entre ambas redes mediante ping.

• Tabla de interfaces del router verificada.

• Proyecto guardado en formato .pkt y documentación en .pdf.

---

## Archivos incluidos

LAB2_INTERCONEXION_DE_LANS_FLOR.pkt → Proyecto de Cisco Packet Tracer

LAB2_INTERCONEXION_DE_LANS_FLOR.pdf → Documentación técnica del laboratorio

---

## Observación

En este laboratorio se utilizó un cable cruzado (crossover) para conectar los switches con el router.

Los equipos Cisco modernos (como el 2960 y el 2911) poseen Auto-MDI/MDIX, lo que permite que tanto cables cruzados como directos funcionen correctamente.

