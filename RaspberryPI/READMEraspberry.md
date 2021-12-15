# ASCENSOR
Modelo NX / Servidor OPC_UA / Data Cloud / Node Red management/ Vision

*************   Vision artificial , librerias OPEN_CV *******************************

Paso a paso:

https://www.pyimagesearch.com/2018/09/26/install-opencv-4-on-your-raspberry-pi/

Imagen completa Raspberry Pi 4 : idekoimh@gmail.com

Para grabarla a una micro SD usar Balena Etcher

Como ejecutar la deteccion de personas:

Primero conectar camara y DESDE TERMINAL ver si la Py la reconoce

`ls -ltr /dev/video*`

Mostrara las camaras:

`crw-rw----+ 1 root video 81, 2 dic 15 13:09 /dev/video15`

`crw-rw----+ 1 root video 81, 1 dic 15 13:09 /dev/video14`

`crw-rw----+ 1 root video 81, 3 dic 15 13:09 /dev/video16`

`crw-rw----+ 1 root video 81, 0 dic 15 13:09 /dev/video13`

hay que probar hasta encontrar cual es .

Para eso cambiar en todas las lineas de codigo de python :

Camara0
`cam = cv2.VideoCapture(0)`
Camara15
`cam = cv2.VideoCapture(15)`
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

`>>> %Run train_model.py`
`[INFO] start processing faces...`

`[INFO] processing image 1/125`

`[INFO] processing image 2/125`

`[INFO] processing image 3/125`

`[INFO] processing image 4/125`

`[INFO] processing image 5/125`


Este analizara todas las fotos de todas las carpetas
Dejar que termine


Para ejecutar el programa de reconocimiento, en el terminal :

` cd facial_recognition` 

` python3 facial_req_email.py` 

https://www.bytefish.de/dev/libfacerec/_images/facerec_video.png



************* Google Spreadsheet API , gestion de  *******************************

Creamos una hoja de calculo en Google Drive

Creamos un proyecto en 

https://console.cloud.google.com/

![This is an image](https://raw.githubusercontent.com/idekoIMH/ASCENSOR/Develop/Captura%20de%20pantalla%202021-12-15%20163128.png)


Habilitamos la API para que nuestro programa en python pueda comunicarse con las hojas de calculo de Drive


![This is an image](https://s3.amazonaws.com/com.twilio.prod.twilio-docs/original_images/google-developer-console.gif)


https://www.twilio.com/blog/2017/02/an-easy-way-to-read-and-write-to-a-google-spreadsheet-in-python.html


Nos descargaremos un archivo .JSON que sera una especie de llave para acceder a la hoja de calculo y la deamos en la misma carpeta donde tengamos los prog. de reconocimiento.
En este caso es /home/pi/facial_recognition

Ahora cargamos librerias en nuestro programa python (facial_req.py)

`import gspread`

`import pandas as pd  #spreadsheet management`

`from oauth2client.service_account import ServiceAccountCredentials`

Definimos las ceredenciales ( archivo JSON ) y nombre de la hoja de calculo (DB_Elevator)

`# define the scope`

`scope = ['https://spreadsheets.google.com/feeds','https://www.googleapis.com/auth/drive']`

`# add credentials to the account`

`creds = ServiceAccountCredentials.from_json_keyfile_name('elevatorimh-d33b18a80991.json', scope)`

`# authorize the clientsheet`

`client = gspread.authorize(creds)`

`# get the instance of the Spreadsheet`

`sheet = client.open('DB Elevator')`

`# get the first sheet of the Spreadsheet`

`DB_Elevator = sheet.get_worksheet(0)`

Nota: sheet.get_worksheet(0) -> quiere decir que accedemos a la PRIMERO HOJA !! Si tuviese mas , cambiar

Ahora podemos Leer/escribir en la hoja de calculo en la nube con las funciones de la libreria:

        `Num_Rows_str = DB_Elevator.acell('L5').value #read cell L5`
        `DB_Elevator.update('N5', '0' ) # write 0 in cell N5`

