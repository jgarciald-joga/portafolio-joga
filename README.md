Instalación de Wazuh - Laboratorio SIEM
📖 Descripción

Este proyecto documenta el proceso de implementación de un sistema SIEM (Security Information and Event Management) utilizando Wazuh.
El laboratorio se compone de:

Máquina virtual con Fedora Server donde se instala el Wazuh Manager.

Máquina virtual con Windows Server, configurada como cliente con Wazuh Agent.

Configuración para la recolección, centralización y análisis de eventos de seguridad.

Este entorno permite aprender sobre monitoreo, correlación de eventos y detección de incidentes, siendo una base para entornos de producción.

🎯 Objetivo

Implementar un laboratorio funcional con Wazuh que permita:

Monitorear registros de seguridad.

Configurar comunicación entre agentes y servidor central.

Detectar eventos críticos en tiempo real.

Mejorar las capacidades de ciberseguridad y respuesta a incidentes.

🗂 Contenido del Proyecto

Instalación de VM Windows Server

Creación de máquina virtual en VirtualBox.

Configuración inicial y conexión a red.

Instalación de VM Fedora Server

Preparación y configuración del sistema base.

Instalación de Wazuh Manager

Despliegue y configuración en Fedora.

Apertura de puertos necesarios en el firewall.

Instalación de Wazuh Agent en Windows

Instalación y vinculación con el Manager.

Validación de envío de eventos.

Pruebas y validación final

Visualización de datos en el dashboard de Wazuh.

🛠 Tecnologías y Herramientas Utilizadas

VirtualBox – Virtualización de servidores.

Fedora Server – Sistema operativo para Wazuh Manager.

Windows Server 2019 – Sistema operativo para cliente con Wazuh Agent.

Wazuh 4.12 – Sistema SIEM.

CLI / PowerShell – Configuración y administración.

🚀 Pasos Rápidos de Instalación

Crear las máquinas virtuales en VirtualBox.

Instalar Fedora y actualizar paquetes:

sudo dnf update -y
sudo dnf install -y curl vim


Instalar Wazuh Manager en Fedora:

curl -sO https://packages.wazuh.com/4.12/wazuh-install.sh && sudo bash ./wazuh-install.sh -a


Configurar firewall para puertos requeridos:

sudo firewall-cmd --permanent --add-port=1514/tcp
sudo firewall-cmd --permanent --add-port=1515/tcp
sudo firewall-cmd --permanent --add-port=1516/tcp
sudo firewall-cmd --permanent --add-port=443/tcp
sudo firewall-cmd --reload


Instalar y vincular Wazuh Agent en Windows Server desde el dashboard.

📊 Resultados

Al finalizar, el laboratorio permite:

Monitorear eventos de seguridad en tiempo real desde Windows Server.

Visualizar alertas en el Dashboard de Wazuh.

Simular escenarios de detección y respuesta ante incidentes.

📌 Capturas de Ejemplo
Windows Server	Wazuh Dashboard

	



📚 Referencias

Documentación oficial de Wazuh

Manual de VirtualBox

Fedora Project

✍ Autor

Jorge García
📍 Santiago, Chile
📧 jorge@mevis.cl

🔗 LinkedIn
