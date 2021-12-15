## INTRODUCCIÓN

* En este documento se explica brevemente la parte integración del modelo de gemelo digital implementado con NX MCD(Mechatronic concept designer en inglés), TiaPortal 16
y PLCSIM advance 3.0.

* El objetivo es poder simular la logica secuencial de funcionamiento del ascensor, y tener un modelo que aparte de que visualize el funciomiento, sea capaz de
interactuar con la lógica de control.

## NX MCD

El archivo de partida es el 3D del ascensor.Posteriormente se migra y filtran las piezas y/o elementos a las extensión PRT
Posteriormente generamos los siguientes elementos de modelo:
* Generamos los cuerpos rígidos de la simulación
* Generamos los ejes y/o actuadores. En este caso es un eje lineal
* Generamos los "sensores" , en este casos sensores se refiere a implementar un control de posición en el eje lineal
* Generamos una señal que posteriormente asociamos a una señal externa de OPCUA.


![image](https://user-images.githubusercontent.com/96112529/146219522-6a8f3eb0-67e5-41e1-a028-d45cfeec1626.png)


## PROGRAMA PLC

El programa de PLC esta implemntado en un controlador Siemens empleando el entorno de TiaPortal 16
Principalmente, la estructura del programa y configuración de PLC se basa en lo siguiente:

* Levantar un servidor OPC-UA para comunicarse de forma bidireccional con NX MCD y Node Red
* Generar un DB Global con las posiciones de ascensor
* Implementar en un bloque funcional la lógica prveniente de Node red
 
## PLCSIM (EJECUCIÓN DE PLC)



