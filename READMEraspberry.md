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

Mostrara las camaras:

hay que probar hasta encontrar cual es .

Para eso cambiar en todas las lineas de codigo de python :

Camara0
`cam = cv2.VideoCapture(0)`
Camara1
`cam = cv2.VideoCapture(1)`
etc

Para crear una persona nueva,primero editar:

`headshots.py`

Cambiar el valor de:

`name = 'Barru' #replace with your name`

Crear una carpeta dentro de dataset con el mismo nombre Barru , etc ...

Y volver a ejecutar (teclaespacio para sacar una foto nueva)

`headshots.py`

Las fotos se guardaran en dataset, en distintas carpetas, distintas personas

Ejecutar:
`train_model.py` 

desde el terminal
Este analizara todas las fotos de todas las carpetas



Dejar que termine


Para ejecutar el programa de reconocimiento, en el terminal :

` cd facial_recognition` 

` python3 facial_req_email.py` 

https://www.bytefish.de/dev/libfacerec/_images/facerec_video.png



************* Google Spreadsheet API , gestion de  *******************************

Creamos una hoja de calculo en excel

Creamos una API para que nuestro programa en python pueda comunicarse con las hojas de calculo de Drive


![This is an image](https://s3.amazonaws.com/com.twilio.prod.twilio-docs/original_images/google-developer-console.gif)


https://www.twilio.com/blog/2017/02/an-easy-way-to-read-and-write-to-a-google-spreadsheet-in-python.html

Seccion : **Obtain service account credentials**

Nos descargaremos un archivo .Json que sera una especie de llave para acceder a la hoja de calculo.

Ahora con las librerias cargadas en nuestro programa python (facial_req.py)

`import gspread`
`import pandas as pd  #spreadsheet management`
`from oauth2client.service_account import ServiceAccountCredentials`




Podemos editar la hoja de calculo en la nube




