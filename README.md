## Índice

1. [Comandos Básicos](#1-comandos-básicos)  
2. [Comandos de Directorios (`cd`)](#2-comandos-de-directorios-cd)  
3. [Comandos de Listas (`ls`)](#3-comandos-de-listas-ls)  
4. [Comandos de Búsquedas](#4-comandos-de-búsquedas)  
5. [Historial de Comandos](#5-historial-de-comandos)  
6. [Comandos para Trabajar con Archivos y Directorios](#6-comandos-para-trabajar-con-archivos-y-directorios)  
7. [Comando de Eliminar (`rm`)](#7-comando-de-eliminar-rm)  
8. [Comando de Concatenar (`cat`)](#8-comando-de-concatenar-cat)  
9. [Comando de Mover (`mv`)](#9-comando-de-mover-mv)  
10. [Buscar con Grep](#10-buscar-con-grep)  
11. [Pipelines o Tuberías](#11-pipelines-o-tuberías)  
12. [Permisos: Comando `chmod`](#12-permisos-comando-chmod)  
13. [Comandos para Trabajar con Grupos](#13-comandos-para-trabajar-con-grupos)  
14. [Propiedades: Comando `chown`](#14-propiedades-comando-chown)  
15. [Atajos de Teclado de la Terminal](#15-atajos-de-teclado-de-la-terminal)  
16. [Comandos para Trabajar con Archivos Largos](#16-comandos-para-trabajar-con-archivos-largos)  
17. [Enlaces Duros y Simbólicos](#17-enlaces-duros-y-simbólicos)  
18. [Nomenclatura de Discos Duros en Linux](#18-nomenclatura-de-discos-duros-en-linux)  
19. [Creación y Administración de Particiones en Linux](#19-creación-y-administración-de-particiones-en-linux)  
20. [Tipos de Particiones de Disco Duro (MBR)](#20-tipos-de-particiones-de-disco-duro-mbr)  
21. [Comandos para Montar Particiones](#21-comandos-para-montar-particiones)  
22. [Montaje Persistente de Discos Duros (`fstab`)](#22-montaje-persistente-de-discos-duros-fstab)

### 1. Comandos Básicos

| Comando | Descripción |
|---|---|
| **`[CTRL] + [+]`** | Acercar el terminal. |
| **`[CTRL] + [-]`** | Alejar el terminal. |
| **`pwd`** | Imprimir el directorio de trabajo actual. |
| **`[CTRL] + [l]`** o **`clear`** | Borrar el contenido de la terminal. |
| **`alias [alias-name]="[comando-a-ejecutar]"`** | Asignar un alias a un comando. |
| **`source [nombre-del-archivo-a-leer-y-ejecutar]`** | Obtener y ejecutar un archivo. |

### 2. Comandos de Directorios (`cd`)

| Comando | Descripción |
|---|---|
| **`cd [nombre-de-tu-directorio]`** | Moverse a un directorio específico. |
| **`cd ..`** | Moverse al directorio principal (padre). |
| **`cd`** o **`cd ~`** | Ir al directorio de inicio del usuario. |
| **`cd -`** | Moverse al último directorio en el que se estaba. |

### 3. Comandos de Listas (`ls`)

| Comando | Descripción |
|---|---|
| **`ls`** | Enumerar todos los archivos y directorios visibles. |
| **`ls -a`** | Enumerar todos los archivos y directorios, incluyendo los ocultos. |
| **`ls -l`** | Mostrar en formato de lista larga (detallado). |
| **`ls -lh`** | Mostrar en formato legible por humanos (tamaños de archivo en KB, MB, GB, etc.). |
| **`ls -lah`** | Combinar argumentos: formato legible por humanos y archivos ocultos. |
| **`man ls`** | Obtener más información sobre el comando `ls`. |

### 4. Comandos de Búsquedas

| Comando | Descripción |
|---|---|
| **`which [nombre-del-programa]`** | Buscar el binario de un programa. |
| **`whereis [nombre-del-programa]`** | Buscar el manual, binario y fuente de un programa. |
| **`find [ruta-de-búsqueda] -iname [nombre-del-archivo-que-quieres-buscar]`** | Buscar archivos y directorios por nombre (ignorando mayúsculas/minúsculas). |
| **`whatis [nombre-del-comando]`** | Obtener una breve descripción de un comando. |
| **`man find`** | Obtener más información sobre el comando `find`. |

### 5. Historial de Comandos

| Comando / Atajo | Descripción |
|---|---|
| **`Up Arrow key ⬆️`** | Obtener comandos anteriores (uno por uno). |
| **`history`** | Obtener una lista completa de comandos anteriores. |
| **`![número-del-comando-a-repetir]`** (después de `history`) | Repetir un comando específico del historial (comando bang). |
| **`!!`** | Repetir el último comando ejecutado (comando bang-bang). |

### 6. Comandos para Trabajar con Archivos y Directorios

| Comando | Descripción |
|---|---|
| **`touch [nombre-de-tu-archivo]`** | Crear un nuevo archivo sin abrirlo. |
| **`vim [nombre-de-tu-archivo]`** o **`nano [nombre-de-tu-archivo]`** | Crear un nuevo archivo usando un editor de texto. |
| **`cp [ruta-de-origen-de-tu-archivo] [ruta-destino-para-tu-archivo]`** | Copiar un archivo. |
| **`mkdir [nuevo-nombre-de-directorio]`** | Crear un nuevo directorio. |
| **`rmdir [nombre-del-directorio-que-quieres-eliminar]`** | Eliminar un directorio vacío. |

### 7. Comando de Eliminar (`rm`)

| Comando | Descripción |
|---|---|
| **`rm [nombre-de-tu-archivo]`** | Eliminar un archivo. |
| **`rm -rf [nombre-de-tu-directorio]`** | Eliminar un directorio de forma recursiva (incluyendo su contenido); usar con precaución. |

### 8. Comando de Concatenar (`cat`)

| Comando | Descripción |
|---|---|
| **`cat [nombre-de-tu-archivo]`** | Ver el contenido de un solo archivo. |
| **`cat -n [nombre-de-tu-archivo]`** | Ver el contenido de un archivo incluyendo los números de línea. |
| **`cat [nombre-del-archivo-del-contenido-a-copiar] > [destination-filename]`** | Copiar el contenido de un archivo a otro archivo. |
| **`man cat`** | Obtener más información sobre el comando `cat`. |

### 9. Comando de Mover (`mv`)

| Comando | Descripción |
|---|---|
| **`mv [ruta-de-origen-de-tu-archivo] [ruta-destino-para-tu-archivo]`** | Mover un archivo de una ubicación a otra. |
| **`mv [nombre-de-tu-archivo] [nuevo-nombre-del-archivo]`** | Cambiar el nombre de un archivo. |

### 10. Buscar con Grep

| Comando | Descripción |
|---|---|
| **`grep [término-a-buscar] [archivo-fuente-de-búsqueda]`** | Buscar una cadena específica dentro de un archivo. |
| **`grep -i [término-a-buscar] [archivo-fuente-de-búsqueda]`** | Búsqueda que no distingue entre mayúsculas y minúsculas dentro de un archivo. |
| **`grep -v [término-a-buscar] [archivo-fuente-de-búsqueda]`** | Buscar líneas que NO coincidan con el término dentro de un archivo. |
| **`grep -r [término-a-buscar] [path-to-directory-to-search]`** | Búsqueda recursiva dentro de un directorio. |
| **`grep -E "[primer-termino-a-buscar|segundo-termino-a-buscar]" [archivo-fuente-de-búsqueda]`** | Realizar varias búsquedas (con OR) dentro de un archivo. |
| **`grep -c [término-a-buscar] [archivo-fuente-de-búsqueda]`** | Contar los resultados de la búsqueda (número de líneas coincidentes). |
| **`grep -l [término-a-buscar] [archivos-que-coincidan-a-buscar]`** | Mostrar solo el nombre de los archivos que contienen el término. |
| **`man grep`** | Obtener más información sobre el comando `grep`. |

### 11. Pipelines o Tuberías

| Descripción                                                             | Comando                                                                 |
|------------------------------------------------------------------------|-------------------------------------------------------------------------|
| Comandos en tuberías                                                   | `comando1 \| comando2 \| comandoN`                                     |
| Canalizar resultados filtrados y guardarlos en un nuevo archivo        | `ls \| grep [término-a-filtrar] \| cat > [ruta]/[nombre-archivo]`      |
| Buscar un término específico en el historial de comandos               | `history \| grep "[término-a-buscar]"`                                 |

### 12. Permisos: Comando `chmod`

| Comando | Descripción |
|---|---|
| **`chmod a+x [nombre-del-archivo]`** o **`chmod +x [nombre-del-archivo]`** | Agregar permiso de ejecución a todos los usuarios. |
| **`chmod a-x [nombre-del-archivo]`** o **`chmod -x [nombre-del-archivo]`** | Quitar el permiso de ejecución a todos los usuarios. |
| **`chmod u+x [nombre-del-archivo]`** | Agregar permiso de ejecución solo al propietario. |
| **`chmod o-w [nombre-del-archivo]`** | Eliminar el permiso de escritura a otros usuarios. |
| **`chmod g+r [nombre-del-archivo]`** | Agregar permiso de lectura al grupo. |
| **`chmod a-wr [nombre-del-archivo]`** | Quitar el permiso de escritura y lectura a todos los usuarios. |
| **`chmod a-wr *.*`** | Quitar el permiso de escritura y lectura a todos para todos los archivos en el directorio actual. |

### 13. Comandos para Trabajar con Grupos

| Comando | Descripción |
|---|---|
| **`getent group`** | Enumerar todos los grupos disponibles en el sistema. |
| **`groups`** | Enumerar todos los grupos a los que está asignada la cuenta actual. |
| **`getent group | grep [nombre-del-grupo-a-buscar]`** | Buscar un grupo específico utilizando tuberías. |
| **`sudo groupadd [nombre-para-el-nuevo-grupo]`** | Crear un nuevo grupo. |
| **`usermod -a -G [grupo-al-que-quieres-agregar-al-usuario] [nombre-usuario-a-agregar]`** | Agregar un usuario existente a un grupo secundario. |

### 14. Propiedades: Comando `chown`

| Comando | Descripción |
|---|---|
| **`sudo chown [nombre-del-nuevo-propietario] [archivo-a-cambiar-su-propiedad]`** | Cambiar la propiedad de usuario para un archivo. |
| **`sudo chown [nombre-del-nuevo-propietario] [file-1-to-change-ownership] [file-n-to-change-ownership]`** | Cambiar la propiedad de usuario para varios archivos. |
| **`sudo chown [nombre-del-nuevo-propietario] [directorio-para-cambiar-propiedad]`** | Cambiar la propiedad de usuario para un directorio. |
| **`sudo chown -R [nombre-del-nuevo-propietario] [directorio-para-cambiar-propiedad]`** | Cambiar recursivamente la propiedad de usuario para un directorio y todos sus archivos. |
| **`sudo chown :[nuevo-nombre-de-grupo] [archivo-a-cambiar-su-propiedad]`** | Cambiar la propiedad de grupo para un archivo. |
| **`sudo chown [nombre-del-nuevo-propietario]:[nuevo-nombre-de-grupo] [archivo-a-cambiar-su-propiedad]`** | Cambiar la propiedad de usuario y grupo de un archivo. |

### 15. Atajos de Teclado de la Terminal

| Atajo | Descripción |
|---|---|
| **`[CTRL] + r`** | Buscar en el historial de comandos. |
| **`[CTRL] + p`** | Pegar líneas anteriores. |
| **`[CTRL] + a`** | Mover el cursor al principio de la línea. |
| **`[CTRL] + e`** | Mover el cursor al final de la línea. |
| **`[CTRL] + f`** | Mover el cursor un carácter hacia adelante. |
| **`[CTRL] + b`** | Mover el cursor un carácter hacia atrás. |
| **`[CTRL] + u`** | Borrar la línea completa. |
| **`[CTRL] + w`** | Borrar la última palabra escrita. |

### 16. Comandos para Trabajar con Archivos Largos

| Comando | Descripción |
|---|---|
| **`tail [nombre-del-archivo]`** | Imprimir las últimas 10 líneas de un archivo. |
| **`tail -n [número-de-líneas] [nombre-del-archivo]`** | Imprimir las últimas `n` líneas de un archivo. |
| **`head [nombre-del-archivo]`** | Imprimir las primeras 10 líneas de un archivo. |
| **`head -n [número-de-líneas] [nombre-del-archivo]`** | Imprimir las primeras `n` líneas de un archivo. |
| **`less [nombre-del-archivo]`** | Ojear un archivo de manera interactiva (permite desplazarse y buscar). |

### 17. Enlaces Duros y Simbólicos

| Tipo de Enlace | Comando de Creación | Características y Restricciones |
|---|---|---|
| **Enlace Duro** | **`ln [ruta-o-nombre-del-archivo-original] [ruta-o-nombre-del-enlace-duro]`** | Se pueden crear solo sobre archivos o ficheros, **NO** en carpetas. Deben estar siempre en la misma partición del disco duro que el archivo original. El comando `cp -rl` también permite crear enlaces duros a cada archivo dentro de una carpeta. |
| **Enlace Simbólico** | **`ln -s [ruta-o-fichero-de-la-carpeta-o-archivo-a-enlazar] [ruta-en-la-que-crearemos-y-nombre-el-enlace-simbólico]`** | Se pueden crear tanto en archivos como en carpetas. Pueden ser creados en cualquier partición o ruta del disco duro. Si el archivo o carpeta al que apunta el enlace se suprime, el enlace queda inutilizable. |

### 18. Nomenclatura de Discos Duros en Linux

| Tipo de Disco Duro | Nomenclatura en Linux |
|---|---|
| **IDE primario maestro** | `hda` (ide0). |
| **IDE primario esclavo** | `hdb` (ide1). |
| **Dispositivos SCSI o discos SATA** | `/dev/sda` o `/dev/scdb`. |

### 19. Creación y Administración de Particiones en Linux

En Linux, puede crear particiones utilizando varias herramientas:

- **`Fdisk`**: Un programa desde la consola para crear particiones. Es útil en servidores sin entorno gráfico. Permite crear particiones primarias y extendidas, y dentro de estas últimas, particiones lógicas. El comando `fdisk -l` muestra el sistema de archivos y los discos. Para trabajar con un disco, se usa `fdisk /dev/sda` (reemplazando `/dev/sda` por el nombre del disco). La ayuda se puede obtener pulsando `m` dentro de `fdisk`. Puede cambiar el tipo de partición con la opción `t` y ver los tipos con `l`. Los cambios se guardan con `w`.

- **`Parted`**: Otro programa desde la consola para particionar discos. Permite particionar un disco en formato GPT. Ejemplos de uso incluyen `parted /dev/sdd` para entrar al disco y `mklabel gpt` para establecer el tipo de tabla de particiones. El comando `mkpart` se usa para crear particiones, especificando nombre, tipo de sistema de ficheros, inicio y fin. Se sale con `quit` o `Ctrl+Z / Ctrl+C`.

- **`GParted`**: Una herramienta con interfaz gráfica para la gestión de discos duros. Se puede instalar desde el Gestor de Paquetes Synaptic en Linux Mint.

### 20. Tipos de Particiones de Disco Duro (MBR)

El **formato** o **sistema de archivo** de una partición (ej. NTFS, ext4) no debe confundirse con el **tipo de partición**. Si se usa un disco duro con **MBR**, existen tres tipos principales de particiones:

- **Partición Primaria**: Son las divisiones principales de un disco. Un disco duro puede tener entre una y cuatro particiones primarias, o hasta tres primarias y una extendida. Un disco físico formateado suele consistir en una única partición primaria que ocupa todo el espacio. Prácticamente, cualquier sistema operativo puede detectar estas particiones si reconoce su formato. Una partición primaria puede ser de arranque y contener un sistema operativo; una de ellas es la **partición activa**, donde el ordenador busca el arranque del sistema. Si hay múltiples sistemas operativos, la partición activa puede contener un **gestor de arranque** (como GRUB).

- **Partición Extendida**: También conocida como partición secundaria, su función principal es contener múltiples unidades lógicas en su interior, superando la limitación de 4 particiones primarias. Solo puede existir una partición de este tipo por disco. A diferencia de las primarias y lógicas, no soporta un sistema de archivos directamente.

- **Partición Lógica**: Ocupa una porción o la totalidad de la partición extendida. Se formatean con un sistema de archivos específico (FAT32, NTFS, ext3, ext4, etc.) y se les asigna una unidad, siendo reconocidas por el sistema operativo. Se pueden tener hasta 23 particiones lógicas en una extendida, aunque Linux impone un máximo de 15 (incluyendo las 4 primarias) en discos SCSI y 8963 en discos IDE.

### 21. Comandos para Montar Particiones

Una vez creadas las particiones, es necesario darles formato y montarlas para poder usarlas:

| Paso | Comando(s) | Descripción |
|---|---|---|
| **1. Dar Formato** | **`mkfs.ext4 /dev/xxx`** o **`mkfs.FormatoElegido /dev/NombrePartición`** | Formatea cada partición con el sistema de archivos deseado (ej., `ext4`). |
| **2. Crear Carpetas de Montaje** | **`cd /mnt/`** luego **`mkdir NombreCarpeta`** (Modo 1) o **`mkdir /mnt/NombreCarpeta`** (Modo 2) | Crea una carpeta que servirá como punto de montaje para la partición. |
| **3. Ejecutar el Montaje** | **`mount -t ext4 /dev/sbdx /mnt/NombreCarpeta`** | Monta la partición especificada (`/dev/sbdx`) en la carpeta creada (`/mnt/NombreCarpeta`). Este comando debe repetirse para cada partición. |
| **4. Comprobar el Montaje** | **`lsblk -f`** o **`df -h`** | Verifica si el montaje se realizó correctamente y muestra el uso de disco. `df -h` muestra los sistemas de archivos y su uso en formato legible por humanos. |
| **5. Desmontar una Partición** | **`umount /mnt/NombreCarpeta`** | Desmonta la partición del punto de montaje. |

### 22. Montaje Persistente de Discos Duros (`fstab`)

Para que las particiones se monten automáticamente cada vez que el sistema se inicia, se deben configurar en el fichero `/etc/fstab`.

| Paso | Comando / Acción | Descripción |
|---|---|---|
| **1. Abrir el fichero `fstab`** | **`nano /etc/fstab`** | Abre el archivo `fstab` con el editor de texto Nano. |
| **2. Agregar Particiones a `fstab`** | Agregar la línea: **`/dev/sdbX /RutaParticion ext4 noatime,nodiratime 0 0`** | Se debe comprobar y anotar previamente la ruta, el nombre de la partición y el formato de archivos. Se usa la tecla TABULACIÓN para separar los campos. Los parámetros `noatime` y `nodiratime` están relacionados con el tiempo de acceso a los archivos. |
| **3. Guardar Cambios y Salir** | **`Control+O`** (Guardar) y **`Control+X`** (Salir) | Atajos de Nano para guardar los cambios y cerrar el editor. |
| **4. Aplicar los Montajes (sin reiniciar)** | **`mount -a`** | Hace que todos los sistemas de archivos mencionados en `fstab` (que cumplan las opciones adecuadas) sean montados, excepto aquellos con la palabra clave `noauto`. |
| **5. Verificar el Espacio en Disco** | **`df -Th`** | Muestra la cantidad de espacio libre en disco y los sistemas de archivos montados, en un formato legible por humanos y mostrando el tipo de sistema de archivo. |

> Es importante tener precaución al modificar el archivo `fstab` y se recomienda realizar pruebas en máquinas virtuales antes de aplicar cambios en entornos de producción.
