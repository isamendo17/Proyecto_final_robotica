# Proyecto Final - Robótica Industrial: Automatización del Proceso de Preparación de Arepas

## Integrantes: 
- Andrés Santiago Cañón Porras
- Juan José Diaz Guerrero
- Cristian Fabian Martínez Bohórquez
- Isabella Mendoza Cáceres

### Descripción de la solución creada, el proceso de alistamiento, herramientas y piezas utilizadas

La solución propuesta consiste en un sistema automatizado para el alistamiento de arepas, integrando un robot industrial Yaskawa con un gripper neumático de dos dedos diseñado por el equipo. El objetivo fue automatizar la toma de las arepas desde una vitrina de almacenamiento hasta su colocación en una parrilla de cocción, como parte del proceso de preparación. El gripper fue diseñado y probado de forma que cumpliera su proposito de agarrar las arepas, y puediera acoplarse con el robot.

En la simulación, realizada con el software correspondiente, se logró ejecutar todo el ciclo: selección de la arepa, traslado, posicionamiento en la parrilla y liberación. Sin embargo, en la implementación física solo se ejecutaron las trayectorias del robot, ya que por razones técnicas no se desmontó el gripper neumático que ya estaba instalado en el robot Yaskawa del laboratorio. Aun así, se verificó que las trayectorias programadas son funcionales y seguras, y que la solución es totalmente viable con el gripper diseñado.

### Diagrama de flujo de las acciones del robot con sus respectivas descripciones

### Descripción, planos y fotografías del gripper diseñado y sus piezas para el proceso de alistamiento

Para este proyecto se diseñó un gripper neumático de dos dedos, pensado para agarrar y mover las arepas automáticamente desde la vitrina de almacenamiento hasta la zona de cocción, incluyendo también el volteo y la entrega final.

<p align="center">
  <img src="https://github.com/user-attachments/assets/8b418f8c-a92b-4e13-9a94-7485c1b65010" alt="Gripper" width="400"/>
</p>

El gripper está hecho por dos partes principales:

- Estructura impresa en PLA: Tanto los dedos como la base del gripper fueron fabricados con impresión 3D usando filamento PLA. Esto ayudó a que fuera liviano, fácil de fabricar y personalizar. Los dedos tienen una forma semicircular que se ajusta muy bien a la forma redonda de las arepas, permitiendo sujetarlas sin dañarlas ni deformarlas.

- Actuador neumático metálico: La única parte metálica es el cilindro neumático de doble efecto, que se encarga de abrir y cerrar los dedos cuando recibe señal desde una electroválvula. Este actuador está bien sujeto a la parte impresa y transmite el movimiento de forma precisa a los dedos.

El gripper se puede montar fácilmente al brazo robótico gracias a una base con orificios. En la parte de atrás se encuentran las conexiones para las mangueras de aire comprimido. En la imagen se ve a la izquierda un objeto cilíndrico cubierto con cinta negra, que usamos como arepa de prueba. Nos sirvió para ensayar el agarre, traslado y liberación de las arepas durante todo el proceso. Así validamos que el gripper funciona correctamente en condiciones reales.

A continuación se adjunta el plano del gripper:

<p align="center">
  <img src="https://github.com/user-attachments/assets/5947d7c0-56a6-42ed-b003-fc083350fe09" alt="Gripper" width="400"/>
</p>

1. Acople del Gripper al Actuador

La siguiente pieza corresponde al acople de unión entre el actuador neumático y la estructura impresa del gripper:

<p align="center">
  <img src="https://github.com/user-attachments/assets/3463745d-144b-4f78-bdea-51ea63d59968" alt="Gripper" width="200"/>
</p>

Esta placa tiene como función principal asegurar el gripper al extremo móvil del actuador, permitiendo que el movimiento del cilindro se transfiera directamente a los dedos de la pinza. Cuenta con múltiples orificios que permiten: La fijación al cuerpo impreso del gripper y el montaje seguro del cilindro neumático mediante tornillos pasantes.

2. Estructura de la Pinza (Dedo Curvo)

La siguiente pieza representa uno de los dedos curvos del gripper, diseñados especialmente para adaptarse a la forma redondeada de las arepas:

<p align="center">
  <img src="https://github.com/user-attachments/assets/bcdc13c2-4558-4191-ac87-3d499db97430" alt="Gripper" width="200"/>
</p>

Este dedo fue fabricado mediante impresión 3D en PLA y tiene un perfil semicircular que permite envolver parcialmente la arepa, brindando un agarre firme y distribuido. La forma curva reduce los puntos de presión directa, evitando que la arepa se deforme o se dañe durante el agarre o traslado. El extremo más recto se conecta con la parte móvil del mecanismo y se articula junto con su par opuesto mediante el movimiento del actuador neumático.

### Modelo en Software de Simulación predeterminado del entorno robótico con todos los elementos que intervienen en el proceso

### Código fuente comentado y discutido del módulo utilizado para el desarrollo del proyecto

### Comparación del tiempo de alistamiento manual y de operación automatizada para las combinaciones seleccionadas

### Vídeo tipo presentación con duración entre 10 a 15 minutos
Debería incluir el clip de introducción de LabSIR, seguido de un banner de la Universidad Nacional de Colombia, autores, profesores, curso, año,
etc. Intro LabSIR, el vídeo debe incluir:
- La simulación en en el software predeterminado con líneas de trazado de trayectorias y cálculo del tiempo total de ensamble. Se debe incluir a la simulación los modelos geométricos de la vitrina, espacio de cocción y arepas.
- Vídeo de implementación del proyecto donde todos los integrantes del grupo participen y expliquen la solución planteada
