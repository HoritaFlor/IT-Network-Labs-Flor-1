# IT-Network-Labs-Flor-1

# Proyecto de red Cisco Packet Tracer  
**Curso:** The Bits and Bytes of Computer Networking (Google)  

**Autor:** Florencia Horita

**Fecha:** 30/10/2025  

---

## Descripción  
Este laboratorio muestra la configuración de una red LAN simple utilizando un **switch Cisco Catalyst 2960** y tres computadoras.  
Se trabajó con asignación de IPs, descripción de interfaces, hostname y verificación de conectividad entre los dispositivos mediante comandos básicos de Cisco IOS.  

---

## Objetivos  
- Comprender el funcionamiento de una LAN (Local Area Network).  
- Configurar un switch Cisco 2960 (IOS 15.0) con hostname e interfaces.  
- Asignar IPs a las PCs y probar comunicación entre ellas.  
- Observar direcciones MAC y tabla de conmutación.  

---

## Topología  
[PC-User1] ---\

[PC-User2] ----> [Switch 2960]

[PC-User3] ---/


---

## Configuraciones principales  
- **IPs:** 192.168.1.2 / 192.168.1.3 / 192.168.1.4  
- **Máscara:** 255.255.255.0  
- **Gateway:** no configurado (red interna sin router)  
- **Hostname del switch:** SW-LAB1  
- **Interfaces configuradas:** FastEthernet 0/1, 0/2, 0/3  

---

## Comandos usados  
```bash
enable
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

## Resultados
- Comunicación exitosa entre todas las PCs mediante ping.
- Tabla MAC del switch correctamente generada.
- Proyecto verificado y guardado en Packet Tracer (.pkt) y PDF (.pdf).

---

## Archivos incluidos  

- `LAB1_LAN_BASICA_FLOR.pkt` → Archivo del laboratorio.  
- `LAB1_LAN_BASICA_FLOR_EN.pdf` → Documentación técnica (bilingüe).  
