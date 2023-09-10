# LeecheRV-Dock_Docs
## *Conexión Serial con el LicheeRV usando minicom*
## Instalar
```
sudo apt install minicom
```
## Usar
```
sudo minicom -s -D /dev/serial/by-id/[Dispositivo conectado]
```
### Se puede listar los dispositivos seriales conectados usando
```
ls /dev/serial/by-id/
```
## En el panel de configuración que aparece en la terminal:

1) seleccionar Serial port setup
2) Inhabilitar Hardware flow control usando la tecla [f] establecer en No
3) Presionar tecla [Enter]
4) Seleccionar opción Exit

Ya. Si todo salió bien se encuentra en el login del LicheeRV 
- [x] Usuario: root
- [x] Pw: licheepi

## Modificación del archivo para habilitar la conexión al usuario root desde SSH conexión
Como root desde la conexión Serial:
1. Usar el comando ``` nano /etc/ssh/sshd_config ```
2. Insertar en una línea "PermitRootLogin yes"
3. [Ctrl+x] para cerrar el archivo
4. [y] para guardar
5. [Enter] para confirmar la ruta de guardado
   
## Conectar el LicheeRV a una red
1. ``` sudoconnmanctl ```
2. ``` enable wifi ```
3. ``` agent on ```
4. ``` scan wifi ```
5. ``` services ``` Lista las redes disponibles
6. ``` connect [Identificador del servicio] ``` El identificador se encuentra en la columna derecha de la lista de services
7. Ingresar la contraseña de la red
8. ```exit```
9. ``` hostname -I ``` Para ver el IP que se le asignó al dispositivo en la red
## Conexión por SSH
Desde una terminal en la máquina personal
- [x] ```sudo ssh -X -l [usuario] [IP asignada a la placa]``` los usuarios disponibles en la imagen que nos entregó el profesor: licheerv, root. Para ambos PW: licheepi
- [ ] Primero pide la contraseña de la maquina anfitrion
- [ ] Luego la del usuario en la placa
#### ***Ya está conectado***
## Descarga de CLion (León marino) 🦁🐋
Link [CLion](https://www.jetbrains.com/es-es/clion/) de [jetbrains](https://www.jetbrains.com/es-es/)
1. Descargar
2. Descomprimir
3. Ubicar la carpeta bin
4. En la terminal ubicado en la carpeta bin ```./clion.sh``` (El programa no es gratuito tiene pruebas gratuitas)
5. O clic derecho en el archivo clion.sh y ejecutar como programa
6. Registrese en la página con una cuenta estudiantil
7. Inicie sesión en el programa con su cuenta ya registrada y que haya solicitado la prueba para estudiantes
#### ***Cree un proyecto en C***
# Instalacion de rsync
Dos opciones: 
* Desde la terminal ```sudo apt install rsync```
* Medio grafico usando: Synaptic Package Manager
# Desarrollando para el sistema embebido
1. Cree un proyecto en C
2. Clic en el engranaje
3. Settings
4. Toolchains
5. Clic en el icono [+]
6. Clic Remote Host
7. Ingresar IP
8. Ingresar usuario
9. Esperar a que se registren las herramientas que de las que dispone el Licheerv
10. En la columna de la izquierda Run targets
11. SSH
12. Repetir pasos 7 y 8

# Para ver los Pines que estan en uso y los disponibles:
Use el comando: ```cat /sys/kernel/debug/pinctrl/2000000.pinctrl/pinmux-pins```
# ----------------------------------------------------------------
~~Intento de traducción del [tutorial](https://bbs.sipeed.com/thread/1300) que se encuentra en la documentación para quemar la imagen en la memoria microSD [wiki sipeed](https://wiki.sipeed.com/hardware/en/lichee/RV/flash.html)~~
# ~~Tabla de contenido~~
  * Introducción a la serie de tableros
  * Tutorial de desempaquetado
  * Empezar a encender
  * Verificación de la función periférica
  * Experiencia espejo de Debian
  * Guía de desarrollo del SDK de BSP
  * Guía de desarrollo de WAFT
## ~~1. Introducción de la serie de placas~~
La serie LicheeRV es la subserie RV de la serie Lichee, principalmente para productos Linux SBC con kernel RISC-V. Actualmente existen los siguientes productos: Nezha CM, HDMI Dock, 86-Panel
## ~~2. Tutorial de desembalaje~~
Los productos LicheeRV comienzan con la tarjeta TF de manera predeterminada, sin importar qué producto compre, primero prepare la tarjeta TF y el lector de tarjetas.
### ~~Software de grabación~~
Dirección de descarga de la herramienta de grabación de tarjetas de imágenes Allwinner: 
Descargue [PhoenixCard.zip](https://dl.sipeed.com/shareURL/LICCHEE/D1/Lichee_RV/tool), descomprímalo y ejecute el programa principal en él
### ~~imagen del sistema~~
La imagen del sistema predeterminada se cargó en el disco de Baidu y se seguirá actualizando.

La imagen del sistema se divide en Tina y Debian: Tina es una imagen pequeña dedicada de Linux y Debian es una imagen de nivel de escritorio.
### ~~configuración de la placa~~
El archivo de configuración de nivel de placa está en el directorio de placa del disco de Baidu mencionado anteriormente. Si el sufijo del paquete inferior (imagen del sistema) no coincide con la placa real, debe usar este archivo fex para sobrescribir la configuración de nivel de placa para mostrar correctamente.
[link de descarga de las imagenes etc](https://mega.nz/folder/lx4CyZBA#PiFhY7oSVQ3gp2ZZ_AnwYA)
