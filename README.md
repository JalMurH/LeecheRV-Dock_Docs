# LeecheRV-Dock_Docs
Intento de traducción del [tutorial](https://bbs.sipeed.com/thread/1300) que se encuentra en la documentación para quemar la imagen en la memoria microSD [wiki sipeed](https://wiki.sipeed.com/hardware/en/lichee/RV/flash.html)
# Tabla de contenido
  * Introducción a la serie de tableros
  * Tutorial de desempaquetado
  * Empezar a encender
  * Verificación de la función periférica
  * Experiencia espejo de Debian
  * Guía de desarrollo del SDK de BSP
  * Guía de desarrollo de WAFT
## 1. Introducción de la serie de placas
La serie LicheeRV es la subserie RV de la serie Lichee, principalmente para productos Linux SBC con kernel RISC-V. Actualmente existen los siguientes productos: Nezha CM, HDMI Dock, 86-Panel
## 2. Tutorial de desembalaje
Los productos LicheeRV comienzan con la tarjeta TF de manera predeterminada, sin importar qué producto compre, primero prepare la tarjeta TF y el lector de tarjetas.
### Software de grabación
Dirección de descarga de la herramienta de grabación de tarjetas de imágenes Allwinner: 
Descargue [PhoenixCard.zip](https://dl.sipeed.com/shareURL/LICCHEE/D1/Lichee_RV/tool), descomprímalo y ejecute el programa principal en él
### imagen del sistema
La imagen del sistema predeterminada se cargó en el disco de Baidu y se seguirá actualizando.

La imagen del sistema se divide en Tina y Debian: Tina es una imagen pequeña dedicada de Linux y Debian es una imagen de nivel de escritorio.
### configuración de la placa
El archivo de configuración de nivel de placa está en el directorio de placa del disco de Baidu mencionado anteriormente. Si el sufijo del paquete inferior (imagen del sistema) no coincide con la placa real, debe usar este archivo fex para sobrescribir la configuración de nivel de placa para mostrar correctamente.
[link de descarga de las imagenes etc](https://mega.nz/folder/lx4CyZBA#PiFhY7oSVQ3gp2ZZ_AnwYA)
