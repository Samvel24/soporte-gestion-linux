# Utilidades de soporte técnico en Linux
Esta guia muestra algunos comandos de Linux que pueden ser de utilidad en diversas aplicaciones y contextos de administración de sistema, en específico en Debian.

## Limpieza de disco y optimización del sistema
* **apt-get clean**: En Debian los paquetes se actualizan con bastante frecuencia y comandos como *apt-get update* y *apt-get upgrade* facilitan bastante el proceso, sin embargo, después de estas actualizaciones quedan algunos archivos que ya no son necesarios, entonces podemos usar clean para eliminar todos los archivos .deb descargados previamente del directorio de caché del paquete (normalmente /var/cache/apt/archives).

* **apt-get autoclean**: Elimina los paquetes almacenados en caché que ya no se pueden descargar. Esto permite evitar que la caché crezca sin control con el tiempo sin vaciarla por completo.

* **apt-get autoremove**: elimina paquetes que se instalaron automáticamente porque otro paquete los requería, pero que, al eliminarse, ya no son necesarios.

## Gestión de tareas
* **nautilus**: El comando nautilus abre el administrador de archivos de GNOME. Permite explorar directorios, administrar archivos e iniciar aplicaciones. Una aplicación útil de este comando es para abrir múltiples ventanas del administrador de archivos para gestionar las diversas tareas o acciones que se deseen realizar en este administrador.

* **history | grep *comando***: Con el comando anterior se puede acceder al historial de comandos de la terminal y después con el operador de flujo de procesamientos (|) se pasa ese texto del historial hacia *grep* para que imprima cada línea que coincide con un patrón, este patrón es el comando que se específica después de escribir grep. Esto puede ser muy valioso cuando se busca un un comando utilizado previamente, de esta manera podemos visualizar todas aquellas veces que utilizamos el comando buscado.

* **tree**: Muestra el árbol de archivos del directorio actual, es de utilidad para buscar carpetas específicas y gestionar el conjunto de directorios de una ubicación deseada.

## Información del sistema
* **uptime -p**: Se utiliza para determinar el tiempo de actividad del sistema. Este comando devuelve un conjunto de valores que incluyen la hora actual y el tiempo que el sistema permanece en ejecución, el número de usuarios conectados y el tiempo de carga de los últimos 1, 5 y 15 minutos, respectivamente.

* **uname -a**: Muestras diversos aspectos del sistema como la arquitectura del sistema operativo, la distribución instalada, etc.

* **free -h**: Proporciona información sobre el uso de la memoria RAM en formato legible.

* **lsblk**: Es una utilidad que permite listar dispositivos de bloque en un sistema Linux. Los dispositivos de bloque son dispositivos de almacenamiento que almacenan datos en forma de bloques, generalmente discos duros (HDD) o unidades de estado sólido (SSD).