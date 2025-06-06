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

📜 Scripts NSE (Nmap Scripting Engine)

### Usar un script individual

nmap --script http-title 192.168.1.1

### Usar una categoría de scripts

nmap --script vuln 192.168.1.1

💡 Otras opciones útiles

### Guardar resultados

nmap -oN scan.txt 192.168.1.1         # salida normal

nmap -oX scan.xml 192.168.1.1         # salida XML

nmap -oA nombrearchivo 192.168.1.1    # todas las salidas (normal, XML, grepable)

### Escaneo con archivo de IPs

nmap -iL lista_ips.txt

### Identificar vulnerabilidades conocidas en el sistema

sudo nmap -f --script vuln 192.168.1.1

### Ejecutar secuencias de comandos menos intrusivas

sudo nmap -f --script safe 192.168.1.1



