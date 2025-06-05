# 🔍 Nmap Cheatsheet

> Nmap (Network Mapper) es una herramienta de código abierto para exploración de red y auditoría de seguridad.

---

## 🛠️ Comandos básicos

### Escaneo rápido

nmap 192.168.1.1

### Escaneo de múltiples host

nmap 192.168.1.1 192.168.1.2 192.168.1.3
nmap 192.168.1.1-10
nmap 192.168.1.0/24

### Escaneo de todos los puertos

nmap -p- 192.168.1.1

### Escaneo de puertos comunes

nmap --top-ports 1000 192.168.1.1

### Detección de versiones

nmap -sV 192.168.1.1

### Detección del sistema operativo

nmap -O 192.168.1.1

### Modo SYN scan (rápido y común)

nmap -sS 192.168.1.1

### Evitar ping para escanear directamente

nmap -Pn 192.168.1.1

### Scan con spoofing de MAC

nmap --spoof-mac Cisco 192.168.1.1



