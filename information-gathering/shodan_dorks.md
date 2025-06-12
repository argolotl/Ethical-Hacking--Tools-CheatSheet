# 🕵️‍♂️ Shodan Dorks Útiles para OSINT y Pentesting

Una recopilación de dorks para Shodan útiles para investigadores, pentesters y entusiastas de la ciberseguridad.

---

## 🎥 Cámaras IP

"Server: GoAhead-Webs"

title:"Live View / - AXIS"

"webcamXP 5"

"uc-httpd"

"IPCam"

"NETSurveillance"

port:554 has_screenshot:true

### 🖥️ Interfaces de Administración

title:"RouterOS Welcome page"

title:"D-Link"

title:"NETGEAR Router"

title:"TP-Link"

http.title:"webmin"

http.favicon.hash:-1372627187  # phpMyAdmin

### 🔐 Autenticación Débil o Deshabilitada

"authentication disabled"

"X-Frame-Options: DENY"

"X-XSS-Protection: 0"

### 📡 Dispositivos IoT

port:23 banner:root

port:2323

port:7547

"Server: Boa/0.94.14rc21"

###  Servicios y Tecnologías Específicas

product:"Apache httpd"

product:"nginx"

product:"OpenSSH"

product:"Microsoft IIS httpd"

"X-Powered-By: PHP"

### 🛠️ Servicios con Posibles Vulnerabilidades

"Apache-Coyote/1.1"

"Server: JBoss"

"Server: CouchDB"

"Server: MongoDB" port:27017

"Elasticsearch" port:9200

"Redis server" port:6379

### 📁 Archivos y Directorios Expuestos

html:"index of /admin"

html:"index of /backup"

html:"index of /conf"

### 🏫 Instituciones Educativas o Gobierno

hostname:.edu

hostname:.gob.mx

org:"Universidad Nacional"

### 📍 Filtrado por Región

country:MX

country:US city:"Los Angeles"

org:"Telmex"

net:"189.203.0.0/16"

### 🧪 Otros Interesantes

ssl:"CN=*.google.com"

ssl:"Let's Encrypt"

asn:8151

### 💡 Combinaciones de Dorks

"Server: GoAhead-Webs" country:MX port:80 has_screenshot:true

⚠️ Nota: Usa estas búsquedas con fines educativos y éticos. Respetar la legalidad es esencial.




