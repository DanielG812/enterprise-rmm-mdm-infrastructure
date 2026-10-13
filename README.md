# Infraestructura Unificada de Gestión de TI (RMM, MDM & RustDesk On-Premises)

Este repositorio documenta la arquitectura e implementación de una solución integral de gestión remota de TI y dispositivos móviles empresariales desplegada sobre Debian 12 con contenedores Docker.

## Arquitectura de la Solución
* Sistema Operativo: Debian 12 (Server)
* Orquestación: Docker & Docker Compose
* RMM (Monitoreo y Gestión): Breeze RMM
* MDM (Gestión de Dispositivos Android): Headwind MDM Community
* Control Remoto Desatendido: Servidor RustDesk OSS (Self-hosted)

## Despliegue Rápido
1. Clona el repositorio:
   git clone [https://github.com/DanielG812/enterprise-rmm-mdm-infrastructure.git](https://github.com/DanielG812/enterprise-rmm-mdm-infrastructure.git)
   cd enterprise-rmm-mdm-infrastructure

2. Configura tus variables a partir de la plantilla:
   cp .env.example .env

3. Inicia los servicios con Docker Compose:
   docker compose up -d
