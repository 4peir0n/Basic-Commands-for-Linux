## 📂 Comandos para el manejo de ficheros

| Comando                                                                                     | Descripción                                  |
| ------------------------------------------------------------------------------------------- | -------------------------------------------- |
| `cat, more, head, tac`                                                                      | listar ficheros (como type)                  |
| `cd`                                                                                        | cambia el directorio                         |
| `compress`                                                                                  | comprime archivos en formato .Z              |
| `cp`                                                                                        | copia un archivo                             |
| `chmod [ugo]+[rwx] target`                                                                  | cambia los permisos de un archivo/directorio |
| `chown usuario.grupo target`                                                                | cambia el propietario del archivo/directorio |
| `df -h`                                                                                     | muestra el espacio libre en disco            |
| `du -sh`                                                                                    | espacio usado por carpeta actual             |
| `du -sh * \| sort -h`                                                                       | ordena carpetas por tamaño                   |
| `ncdu`                                                                                      | analiza uso de disco                         |
| `ncdu /usr`                                                                                 | sobre /usr                                   |
| `fdformat`                                                                                  | formatea disquete                            |
| `fdisk`                                                                                     | particiona unidades                          |
| `file`                                                                                      | tipo de archivo por análisis parcial         |
| `find directorio -name match`                                                               | búsqueda recursiva                           |
| `find . -name "texto*"`                                                                     | búsqueda desde directorio actual             |
| `find . -name "texto*" -name "*U*" -printf "%T@\t%Tc %6k KiB %p\n" \| sort -n \| cut -f 2-` | búsqueda avanzada con filtros                |
| `fsck`                                                                                      | chequeo del sistema de archivos              |
| `grep`                                                                                      | búsqueda en ficheros                         |
| `gzip`                                                                                      | comprimir/descomprimir GZip                  |
| `ln -sf /dev/ttyS0 /dev/mouse`                                                              | enlace simbólico                             |
| `ln -sf /dev/ttyS1 /dev/modem`                                                              | enlace simbólico                             |
| `ls`                                                                                        | listar directorios                           |
| `ls -l --full-time`                                                                         | formato completo                             |
| `ls -X / -t / -S`                                                                           | orden por extensión / fecha / tamaño         |
| `mkdir`                                                                                     | crear directorio                             |
| `mkfs`                                                                                      | crear nuevo sistema de archivos              |
| `mkswap`                                                                                    | crear espacio swap                           |
| `more`                                                                                      | mostrar contenido de archivo                 |
| `mount`                                                                                     | montar unidad                                |
| `mv`                                                                                        | mover/renombrar archivos                     |
| `pwd`                                                                                       | mostrar directorio actual                    |
| `rm`                                                                                        | borrar archivos                              |
| `rmdir`                                                                                     | borrar directorio vacío                      |
| `rm -r`                                                                                     | borrar directorio con contenido              |
| `split`                                                                                     | partir ficheros                              |
| `swapon`                                                                                    | activar swap                                 |
| `swapoff`                                                                                   | desactivar swap                              |
| `tar`                                                                                       | empaquetar/desempaquetar .tar                |
| `touch`                                                                                     | modificar fecha                              |
| `type`                                                                                      | mostrar ubicación del ejecutable             |
| `umount`                                                                                    | desmontar unidad                             |
| `byobu`                                                                                     | compartir consola                            |
| `dd if=/dev/zero of=test.img bs=1MB count=4096`                                             | crear archivo de 4GB con ceros               |
| `scp -P PUERTO archivo usuario@host:path`                                                   | copiar archivos con SSH                      |

> **Opciones de `cp`:**
>
> * `-R`: recursivo
> * `-p`: mantener permisos, propietario, grupo y marcas de tiempo

---

## ⚙️ Comandos para el manejo de procesos

| Comando              | Descripción                                 |
| -------------------- | ------------------------------------------- |
| `kill PID`           | enviar señal a proceso                      |
| `killall nombre`     | matar todos los procesos con el nombre dado |
| `ps aux`             | mostrar todos los procesos del sistema      |
| `ps -eF`             | formato extendido                           |
| `top`                | lista de procesos en ejecución              |
| `htop`               | versión interactiva mejorada de top         |
| `jobs`               | ver trabajos en segundo plano               |
| `bg`                 | reanudar en segundo plano                   |
| `fg`                 | traer a primer plano                        |
| `nice -n 10 comando` | ejecutar con prioridad modificada           |
| `renice +10 PID`     | cambiar prioridad de proceso                |

---

## 🌐 Comandos para el manejo de red

| Comando                     | Descripción                       |
| --------------------------- | --------------------------------- |
| `ping dominio`              | enviar paquetes ICMP              |
| `traceroute dominio`        | trazado de ruta                   |
| `netstat -tulnp`            | conexiones y puertos escuchando   |
| `ss -tuln`                  | alternativa moderna a netstat     |
| `ip addr show`              | mostrar interfaces de red         |
| `ip route`                  | mostrar tabla de rutas            |
| `curl http://url`           | realizar peticiones HTTP          |
| `wget url`                  | descargar archivos desde Internet |
| `ftp servidor`              | conectar a servidor FTP           |
| `scp archivo usuario@host:` | copiar vía SSH                    |
| `rsync -avz origen destino` | sincronización remota/local       |
| `nmap IP`                   | escaneo de puertos                |

---

## 👤 Comandos para el manejo de usuarios

| Comando                     | Descripción                        |
| --------------------------- | ---------------------------------- |
| `adduser nombre`            | crear nuevo usuario                |
| `userdel nombre`            | eliminar usuario                   |
| `usermod -aG grupo usuario` | añadir usuario a grupo             |
| `passwd usuario`            | cambiar contraseña                 |
| `who`                       | mostrar quién está conectado       |
| `id`                        | mostrar UID y grupos de un usuario |
| `groups usuario`            | mostrar grupos del usuario         |
| `su usuario`                | cambiar de usuario                 |
| `sudo comando`              | ejecutar como root                 |

---

## 🔧 Comandos para servicios y demonios (systemd)

| Comando                               | Descripción              |
| ------------------------------------- | ------------------------ |
| `systemctl status servicio`           | estado del servicio      |
| `systemctl start servicio`            | iniciar servicio         |
| `systemctl stop servicio`             | detener servicio         |
| `systemctl restart servicio`          | reiniciar servicio       |
| `systemctl enable servicio`           | activar al inicio        |
| `systemctl disable servicio`          | desactivar al inicio     |
| `systemctl list-units --type=service` | listar servicios activos |

---

## 🌍 Comandos para Apache y MySQL

| Comando                     | Descripción            |
| --------------------------- | ---------------------- |
| `systemctl status apache2`  | estado Apache          |
| `systemctl restart apache2` | reiniciar Apache       |
| `a2ensite sitio`            | habilitar sitio        |
| `a2dissite sitio`           | deshabilitar sitio     |
| `mysql -u root -p`          | acceder a MySQL        |
| `SHOW DATABASES;`           | mostrar bases de datos |
| `SHOW TABLES;`              | mostrar tablas         |
| `CREATE DATABASE nombre;`   | crear base de datos    |
| `DROP DATABASE nombre;`     | eliminar base de datos |

---

## 📑 Otros útiles

| Comando                     | Descripción                    |
| --------------------------- | ------------------------------ |
| `man comando`               | manual del comando             |
| `history`                   | historial de comandos          |
| `alias nombre='comando'`    | alias temporal                 |
| `nano archivo`              | editor de texto simple         |
| `vim archivo`               | editor avanzado                |
| `apt install paquete`       | instalar paquete Debian/Ubuntu |
| `apt update && apt upgrade` | actualizar sistema             |
| `dpkg -i paquete.deb`       | instalar archivo .deb          |

---
