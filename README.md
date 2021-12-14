# ASCENSOR
Modelo NX / Servidor OPC_UA / Data Cloud / Node Red management/ Vision

*************   Vision artificial , librerias OPEN_CV *******************************

Paso a paso:

https://www.pyimagesearch.com/2018/09/26/install-opencv-4-on-your-raspberry-pi/

Imagen completa Raspberry Pi 4 : idekoimh@gmail.com

Para grabarla a una micro SD usar Balena Etcher

Como ejecutar la deteccion de personas:

Primero conectar camara y ver si la Py la reconoce

`ls -ltr /dev/video*`

Mostrara las camaras. hay que probar hasta encontrar cual es .

Para eso cambiar en todas las lineas de codigo:

`cam = cv2.VideoCapture(0)`

Para crear una persona nueva, editar:

`headshots.py`

Cambiar el valor de:

`name = 'Barru' #replace with your name`

Crear una carpeta dentro de dataset con el mismo nombre Barru , etc ...

Y volver a ejecutar (teclaespacio para sacar una foto nueva)

Las fotos se guardaran en dataset, en distintas carpetas

Ejecutar:
`train_model.py` 

desde el terminal
Este analizara todas las fotos de todas las carpetas
Dejar que termine
