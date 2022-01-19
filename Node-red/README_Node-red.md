

## Introducción

En este README se va a explicar todo lo que se ha realizado en Node-red, explicando paso a paso todas las configuraciones y por otro lado, también se va a explicar la utilización de la herramienta tecnológica DOCKER.

## INSTALACIONES
Cabe destacar que hay varias vías para tener Node-red instalado: 
* **Localmente**: se puede instalar Node-red localmente siguiendo los siguentes pasos:
  - 1- Instalando Node js mediante la URL ---> (https://nodejs.org/es/).
  - 2- Ejecutando el comando 'npm install -g --unsafe-perm node-red' para instalar Node-red.
  - 3- Correr la aplicación - **in a terminal window** -> npm node-red.

* **Mediante Docker**: Accediendo a la página oficial de Docker (https://www.docker.com/products/docker-desktop).
  - 1- Una vez que tenemos instalado Docker en nuestro pc, se habre el terminal y se introduce el comando `docker pull nodered/node-red-docker` para descargarnos la última imagen de node-red.
  
     ![image](https://user-images.githubusercontent.com/96112529/150083438-bec436d1-8b58-428a-bcce-23a4c1535977.png)
     
  - 2- Después de descargarnos la imagen, montamos un contenedor, es decir, una aplicación con la imagen de Node-red. Para eso ejecutamos el comando `docker run -it -p 1880:1880 -v node_red_data:/data --name Node-Red nodered/node-red`

## CONFIGURACIONES
Una vez que está instalado la aplicación de node-red en nuestro pc, ya sea localmente o mediante DOCKER, accedemos a la aplicación.

Acceso mediante la URL --------> localhost:1880

De esta forma se accede a la aplicación y aparecerá el entorno de programación por nodos llamado "Flow 1" vacío, con lo cual, para que se importen los nodos de este proyecto lo que se hará es:

  - 1- Descargar el JSON del proyecto llamado `Elevator_Ermua_Flow.json` dentro del directorio `/Node-red´.
  - 2- Importar el fichero JSON dentro de Node-red.
  
  ![image](https://user-images.githubusercontent.com/96112529/150155392-bbf1070c-9d85-4022-9c28-e920b805ddac.png)

  - 3- Puede que haya algún problema a la hora de importar el JSON y es que seguramente se no aparezcan las librerías descargadas de esos nodos. Para eso, lo que se tendrá que hacer es descargarlos en el apartado "Manage Palette". 

![image](https://user-images.githubusercontent.com/96112529/150157904-4cedada8-d36e-46a8-a295-fbda18b96e8d.png)

Una vez descargado correctamente la librerías que falten, ya se puede configurar los nodos a nuestro antojo.

![image](https://user-images.githubusercontent.com/96112529/150156974-650d6da3-b62c-492a-9380-f7b571e02ce6.png)



## MAINTAINERS

* Aitor Barrutia: - a.barrutia@ideko.es
* Jose Luis Bellanco - jlbellanco@ideko.es
* Joseba García - jgarciabilbao@ideko.es
