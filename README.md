# 🚀 Infraestructura Unificada On-Premises: RMM, MDM & Control Remoto

![Debian 12](https://img.shields.io/badge/OS-Debian%2012-A81D33?style=flat-square&logo=debian&logoColor=white)
![Docker](https://img.shields.io/badge/Orchestration-Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Breeze RMM](https://img.shields.io/badge/RMM-Breeze-blue?style=flat-square)
![Headwind MDM](https://img.shields.io/badge/MDM-Headwind-green?style=flat-square)
![RustDesk](https://img.shields.io/badge/Remote-RustDesk-orange?style=flat-square)

Repositorio oficial que documenta la arquitectura, diseño y despliegue de una solución integral de infraestructura de TI centralizada y autohospedada (On-Premises), orientada a la gestión unificada de estaciones de trabajo, servidores y dispositivos móviles corporativos de forma segura y automatizada.

---

## 📐 Arquitectura de la Solución

La infraestructura opera sobre un servidor dedicado con **Debian 12**, utilizando contenedores **Docker** y un Proxy Inverso HTTPS para garantizar aislamiento de servicios, escalabilidad y seguridad perimetral.

```text
       Internet / Red Externa (IP Pública)
                 │
      [ Firewall / MikroTik ] (NAT / Puertos 80, 443)
                 │
       [ Servidor Debian 12 ] (IP LAN: 192.168.176.221)
                 │
     [ Nginx Proxy Manager ] (Reverse Proxy & SSL Let's Encrypt)
         │               │              │
         ├──────► [ Breeze RMM ]        │ (Supervisión de PCs y Servidores)
         ├──────► [ Headwind MDM ]      │ (Gestión de Dispositivos Android / Kiosk)
         └──────► [ RustDesk Server ]   │ (Control Remoto Desatendido OSS)
