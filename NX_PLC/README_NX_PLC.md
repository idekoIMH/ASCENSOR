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

## PROGRAMA PLC

El programa de PLC esta implemntado en un controlador siemens empleando el entorno de TiaPortal 16
Principalmente 
