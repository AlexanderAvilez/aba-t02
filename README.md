# TAREA 02


| Código | Description |
| ------:| ----------- |
| ***Asignatura*** | Código del Trabajo o Número de Tarea | 
| **TSR-2022-I** | *3090* |
| **Robotica-2022-I**  | Tarea *02* |
| **IT102321-C002** | Sistema Ciber-Físico - Proyecto - Módulo |

## Contenido

- [Objetivo](#objetivo)
- [Introducción](#introduccion)
- [Desarrollo](#desarrollo)
- [Conclusiones](#conclusiones)
- [Autor](#autor)
- [Referencias](#referencias)

## Objetivo

Investigación. Investigar los diferentes sensores que componen al robot Robotis Turtlebot3 Waffle y su transmisión de datos en ROS (nodos, tópicos, servicios, simulaciones).
Simulación: Mover al robot de su posición inicial a un punto dado de coordenadas (X, Y).

## Introducción
La importancia de estudiar la optimización de trayectorias permite avanzar en investigaciones sobre
decisiones que tomaría un robot de forma autónoma para trasladarse de un terreno con muchos obstáculos 
y finalmente llegar hacia su objetivo final. Además, permite conocer resultados en la utilización de 
algoritmos que se asocien al continuo funcionamiento de robots que solucione la optimización de trayectorias 
que puedan cumplir su objetivo en el menor tiempo posible.

En la actualidad se está estudiando automóviles eléctricos autónomos que tomen decisiones
dentro de una ciudad con obstáculos. Estos automóviles eléctricos realizan un continuo
reconocimiento del lugar donde transita, analizando los obstáculos durante su trayecto. Para su
funcionamiento define su destino y la ruta de menor longitud y mayor facilidad de recorrido.
En la actualidad existen brazos robóticos pertenecientes a la compañía ABB que realizan
tareas autónomas y repetitivas, en las cuales calculan su recorrido de desplazamiento para tener
adecuada movilidad en la toma de decisiones que requiere mayor precisión y menor tiempo de
funcionamiento. Este robot calcula su ubicación inicial junto con el recorrido que debe realizar
para llegar a su objetivo final. 

Turtlebot3.

Turtlebot3 consiste en una idea de varios módulos de platos que usuarios puede escoger a
partir de su forma. El turltebot3 viene en tres tipos: Burger, waffle y waffle Pi. Cada uno tiene una
forma distinta en tamaño y en funcionalidad.
El turtlebot3 consiste en una base, dos motores dynamixel, una batería de 1800mA, un sensor
lidar de 360 grados de giro, una cámara (cámara “Real Sense” para wiffle y cámara rasberry pi
para waffle pi), una SBC (computador de una sola placa: rasberry pi 3 tipo B y Intel Joule 570X)
y un kit para montaje y construcción para adición de más sensores. Los tipos de robot turtlebot3
fue creado en mayo del año 2017
![Turtlebot3](https://www.roscomponents.com/1326-thickbox_default/turtlebot3-burger.jpg "Turtlebot3")

## Desarrollo

####Transmisión de datos
#####Nodos, tópicos y servicios
Un nodo en realidad no es más que un archico ejecutable dentro de un paquete de ROS. Los nodos
de ROS utilizan una biblioteca cliente para comunicarse con otros nodos. Los nodos pueden publicar 
o suscribirse a un topic. Los nodos pueden utilizar o proporcionar algún servicio.
- Rosnode
rosnode muestra información sobre los nodos de ROS que se están ejecutando. El comando rosnode list lista 
los nodos que están activos.
El comando rosnode info devuelve información sobre un nodo específico.
- Rosrun
rosrun permite usar el nombre del paquete para ejecutar directamente un nodo (sin necesidad de conocer la ruta del paquete).

```
$ rosrun [package_name] [node_name]
```
- Tópico (topic):
Son canales de información entre los nodos. Un nodo puede emitir o suscribirse a un tópico. Por ejemplo, 
stage (simulador de robots) emite un tópico que es la odometría del robot. Cualquier nodos se puede suscribir. 
El nodo que emite no controla quién está suscrito. La información es, por tanto, unidireccional (asíncrona). 
Si lo que queremos es una comunicación síncrona (petición/respuesta) debemos usar servicios.
Un tópico no es más que un mensaje que se envía. Podemos usar distintos tipos de clases de mensajes.
Los tópicos son acciones más específicas que el sistema pueda acceder en cada nodo. Cada
nodo puede tener más de un tópico. Cuando uno nodo está en funcionamiento se asocia a un tópico
que permitirá realizar una tarea de manera específica a través de ordenes por medio de mensajes.
Los mensajes son asociados a “suscripción y publicador” en ROS. La suscripción es el
encargado de etiquetan a un tópico con el nodo y acceder a información entre nodos y tópicos. El
publicador es el encargado de permitir ver la información asociada a un nodo o tópico para
visualizarse o realizar alguna tarea.
Gráficamente los nodos son escritos con una circunferencia y los tópicos con un rectángulo,
construidos a partir de la ejecución de archivos c++ o Python.
- Servicios
![Servicios](https://geekgasteiz.files.wordpress.com/2018/03/captura-de-pantalla-2018-03-17-a-las-9-58-09.png"Diagrama de servicios ROS")

Un servicio es un tipo de comunicación de ROS en el que pasamos un mensaje y nos devuelve una respuesta.
Un ejemplo de un servicio en una aplicación robótica, puede ser el de una aplicación en el que el usuario 
envía el tipo de pieza que se quiere localizar, request, y el servicio devuelve la localización de ese tipo de pieza, response.


En los servicios distinguimos dos partes bien diferenciadas, por un lado está el nodo cliente, que es el nodo en el cual se 
realiza la petición, el nodo que envía el “request”, y el nodo servidor, que es el que realiza la operación y devuelve una respuesta, 
devuelva la “response”.
#####Sensores del robot Robotis Turtlebot3 Waffle 
1. 360 Laser Distance Sensor LDS-01
2. Raspberry Pi Camera Module v2.1
3. Gyroscope 3 Axis
4. Accelerometer 3 Axis
5. Magnetometer 3 Axis

## Conclusiones
Me ayudo a comprender de una mejor manera los temas que habíamos visto anteriormente en clase, especialmente el tema de los
servicios, ese tema es el que más me ha costado comprender y al buscar información y algunos ejemplos qu epude ver en la investigación
me quedo a clarificar mis dudas.

## Autor

**Autor** Avilez Bahena Alexander [GitHub profile](https://github.com/AlexanderAvilez)

## Referencias

_Referencia simple_

<a id="1">[1]</a> https://moodle2018-19.ua.es/moodle/mod/book/tool/print/index.php?id=8465#ch186

<a id='2'>[2]</a>	https://www.roscomponents.com/es/robots-moviles/214-turtlebot3-burger.html#/cursos-no/turtlebot_3_burger_modelo-burger_intl_

<a id="3">[3]</a>  http://rostutorial.com/7-servicios/
