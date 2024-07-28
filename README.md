# OVA para Desarrollo y Testing de Aplicaciones PHP con CodeIgniter 3.1.13

Esta OVA está configurada para facilitar el desarrollo y testing de aplicaciones PHP basadas en el framework CodeIgniter 3.1.13 en entornos locales. La configuración está diseñada para ser usada en un entorno de desarrollo y no incluye configuraciones de VHOSTs, IPTables ni SSL para evitar complicaciones innecesarias en este contexto.

## Características de la OVA

- **Sistema Operativo:** Ubuntu 24.04 LTS
- **Servidor Web:** Apache 2.4.62
- **Lenguaje de Programación:** PHP 8.3
- **Framework:** CodeIgniter 3.1.13
- **Base de Datos:** MySQL 8.3.9
- **Acceso Sesión, SSH y MySQL:**
  - **Usuario:** `devadmin`
  - **Contraseña:** `d3v4dm1n`

## Descargar, Acceso y Uso

Antes de nada, es necesario descargar la OVA, para ello haz click en el siguiente enlace:
[Desarrollo de Aplicaciones con CI 3.1.13.ova](https://mega.nz/file/5oJCEYja#M6ICl_uhYz6b5lHPucNpQq7NyWLixTW-Eh0pOLeUcxI)

Para poder hacer uso de esta OVA, es necesario importarla en un Virtualbox o VMware, y configurar la interfaz de red como NAT o otra de las opciones. Una vez se configure y arranque la VM, se deberá acceder con las credenciales de Sesión, y, para obtener la dirección IP de la máquina, ejecutar el comando

```bash
ip a
```

### SSH

Para acceder a la máquina virtual a través de SSH, utiliza las siguientes credenciales:

- **Usuario:** `devadmin`
- **Contraseña:** `d3v4dm1n`

```bash
ssh devadmin@<IP-de-la-OVA>
```

### MySQL

Para acceder a MySQL:

```bash
mysql -u devadmin -p
```

### Entorno de trabajo

El entorno de trabajo se ubica en el directorio `/var/www/html`, la cual se divide en:

- `/var/www/html/sql`: para el gestor de base de datos (PHPMyAdmin 5.2.1), accesible mediante la URL: http://<IP-de-la-OVA>/sql/
- `/var/www/html/public`: para el codeigniter 3.1.13, accesible mediante la URL: http://<IP-de-la-OVA>/public/

### Apache

La configuración de Apache está preparada para servir el proyecto desde el directorio `/var/www/html`. No es necesario modificar configuraciones de VHOSTs para el entorno de desarrollo.

### PHP

La OVA incluye PHP 8.3 con las extensiones necesarias para ejecutar CodeIgniter y otras aplicaciones web comunes. Si necesitas instalar extensiones adicionales, puedes hacerlo usando `apt`.

```bash
sudo apt  install php-<extension>
```

## Notas Adicionales

- Esta OVA está configurada para entornos locales y no se recomienda su uso en producción.
- Para cualquier problema o pregunta, contacta conmigo.

## Licencia

Esta OVA se proporciona tal como está, sin garantías de ningún tipo. Usa bajo tu propia responsabilidad.
