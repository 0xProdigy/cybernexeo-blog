---
title: "Linux Hardening Check - Script de auditoría de seguridad"
date: 2026-06-04 10:00:00 -0500
categories: [Herramientas, Linux]
tags: [linux, hardening, python, seguridad, auditoria]
author: 0xProdigy
pin: true
---

## ¿Qué es linux-hardening-check.py?

Script en Python que realiza verificaciones clave de seguridad en sistemas 
Linux. Pensado para auditorías rápidas, validación de buenas prácticas y 
revisiones post-instalación. Con salida colorida y logs completos.

> Este [script](). **no realiza cambios en el sistema**, solo audita.
{: .prompt-info }

## Verificaciones incluidas

- Permisos de archivos críticos: `/etc/passwd`, `/etc/shadow`, `/etc/group`
- Usuarios con UID 0 distintos de `root`
- Expiración de contraseñas no configurada
- Servicios inseguros activos (`telnet`, `ftp`, `rsh`)
- Acceso SSH como `root` habilitado
- Binarios con bit SUID
- Firewall activo (`ufw`, `iptables`)
- Registros recientes de login y escaladas

## Requisitos

- Python 3.x
- Acceso como `root` para resultados completos

## Uso

```bash
sudo python3 linux_hardening_check.py
```

> Se recomienda ejecutar como root para obtener resultados completos.
{: .prompt-warning }

## Conclusión

Una herramienta útil para cualquier sysadmin o pentester que quiera 
verificar rápidamente el estado de hardening de un sistema Linux sin 
modificar nada.