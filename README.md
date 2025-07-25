# Proyecto Final - Robótica Industrial: Automatización del Proceso de Preparación de Arepas

## Integrantes: 
- Andrés Santiago Cañón Porras
- Juan José Diaz Guerrero
- Cristian Fabian Martínez Bohórquez
- Isabella Mendoza Cáceres

### Descripción de la solución creada, el proceso de alistamiento, herramientas y piezas utilizadas

A manera de bitácora del desarrollo del proyecto. No olviden ser detallados y describir el proceso como quieren que
sea visto para sus pares.

### Diagrama de flujo de las acciones del robot con sus respectivas descripciones

### Descripción, planos y fotografías del gripper diseñado y sus piezas para el proceso de alistamiento

Para este proyecto se diseñó un gripper neumático de dos dedos, pensado para agarrar y mover las arepas automáticamente desde la vitrina de almacenamiento hasta la zona de cocción, incluyendo también el volteo y la entrega final.

<p align="center">
  <img src="https://github.com/user-attachments/assets/8b418f8c-a92b-4e13-9a94-7485c1b65010" alt="Gripper" width="600"/>
</p>

El gripper está hecho por dos partes principales:

- Estructura impresa en PLA: Tanto los dedos como la base del gripper fueron fabricados con impresión 3D usando filamento PLA. Esto ayudó a que fuera liviano, fácil de fabricar y personalizar. Los dedos tienen una forma semicircular que se ajusta muy bien a la forma redonda de las arepas, permitiendo sujetarlas sin dañarlas ni deformarlas.

- Actuador neumático metálico: La única parte metálica es el cilindro neumático de doble efecto, que se encarga de abrir y cerrar los dedos cuando recibe señal desde una electroválvula. Este actuador está bien sujeto a la parte impresa y transmite el movimiento de forma precisa a los dedos.

El gripper se puede montar fácilmente al brazo robótico gracias a una base con orificios. En la parte de atrás se encuentran las conexiones para las mangueras de aire comprimido. En la imagen se ve a la izquierda un objeto cilíndrico cubierto con cinta negra, que usamos como arepa de prueba. Nos sirvió para ensayar el agarre, traslado y liberación de las arepas durante todo el proceso. Así validamos que el gripper funciona correctamente en condiciones reales.

A continuación se adjunta el plano del gripper:

<p align="center">
  <img src="https://github.com/user-attachments/assets/5947d7c0-56a6-42ed-b003-fc083350fe09" alt="Gripper" width="400"/>
</p>

### Modelo en Software de Simulación predeterminado del entorno robótico con todos los elementos que intervienen en el proceso

### Código fuente comentado y discutido del módulo utilizado para el desarrollo del proyecto

### Comparación del tiempo de alistamiento manual y de operación automatizada para las combinaciones seleccionadas

### Vídeo tipo presentación con duración entre 10 a 15 minutos
Debería incluir el clip de introducción de LabSIR, seguido de un banner de la Universidad Nacional de Colombia, autores, profesores, curso, año,
etc. Intro LabSIR, el vídeo debe incluir:
- La simulación en en el software predeterminado con líneas de trazado de trayectorias y cálculo del tiempo total de ensamble. Se debe incluir a la simulación los modelos geométricos de la vitrina, espacio de cocción y arepas.
- Vídeo de implementación del proyecto donde todos los integrantes del grupo participen y expliquen la solución planteada
