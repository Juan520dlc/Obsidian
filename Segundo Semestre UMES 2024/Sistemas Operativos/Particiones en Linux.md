### Particiones
Cuando halamos de particiones nos referimos a la forma en que dividimos nuestro disco con respecto a la memoria
Linux utiliza 3 particiones:
- El directorio raíz:
	- Es el punto de partida principal en la jerarquía del sistema de archivos Linux
	- Cualquier ruta de archivo en Linux comienza con el directorio raíz
- Partición SWAP:
	- Esta es una partición para intercambio de memoria
	- Esta se utiliza como un área de almacenamiento para archivos temporales de la memoria RAM
	- Permite que el SO emplee la memoria virtual, que es una combinación de la memoria RAM y la partición swap, para ejecutar aplicaciones y procesos
- Directorio Home:
	- Es el directorio principal, en el que se almacenan las carpetas personales de los usuarios
	- Cada usuario tiene una carpeta de inicio dentro de /home

## Particiones en el disco duro
- El SO decide el número de Clusters
- Particionar el disco duro permite instalar distintos sistemas operativos en la misma unidad. Por esta razón el usuario puede seleccionar con qué sistema operativo desea iniciar.
- El sistema operativo gestiona las particiones por medio de un registro llamao MBR (Master Boot Record)
- Ña MBRS ha tenido diferentes modificaciones, es decir, otra tabla de particiones llamdas GUID o GPT, la cual permite realizar a los discos duros más particiones y acomodar discos más grandes.
### Tareas que realiza el MBR
1. Registro principal de arranque o registro del arranque maestro
2. COntiene la información acerca de las particiones de esa unidad
3. Utiliza la BIOS y las direcciones físicas de la unidad de disco para especificar las particiones
#### MBR
- Es compatible con todos los sisteas operativos
- Utiliza la tabla de particiones estándar en la zona cero del disco duro
- Se establece por defecto en los dispositivos de almacenamiento móviles como las memorias de
### GPT
- GPT es comptable en linux  a paerie 2003
- Soporta discos de 256 TB en una sola partición, MBS rolo soporta discos de 2 TB.
- Utiliza EFI (Extensible Firmware Interface) en lugar de la tabla de particiones estándar en la BIOS, pero es necesario que la BIOS implemente esta característica
- Soporta 128 particiones primarias, mientras que MBR solo soporta 4 particiones primarias o 3 primarias y 1 extendida con hasta 128 volúmenes lógicos.
#### Pistas
El disco duro esta dividido en pistas
#### Cluster
Conjunto de sectores
#### Plato
Es cada circulo
