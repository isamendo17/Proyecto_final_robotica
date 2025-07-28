# Proyecto Final - Robótica Industrial: Automatización del Proceso de Preparación de Arepas

## Integrantes: 
- Andrés Santiago Cañón Porras
- Juan José Diaz Guerrero
- Cristian Fabian Martínez Bohórquez
- Isabella Mendoza Cáceres

### Descripción de la solución creada, el proceso de alistamiento, herramientas y piezas utilizadas

<p align="center">
  <img src="https://github.com/user-attachments/assets/e89ae91d-e61f-4ee9-9377-9af222923d6c" alt="Gripper" width="400"/>
</p>

La solución propuesta consiste en un sistema automatizado para el alistamiento de arepas, integrando un robot industrial Yaskawa con un gripper neumático de dos dedos diseñado por el equipo. El objetivo principal fue automatizar la toma de las arepas desde una vitrina de almacenamiento y colocarlas sobre una parrilla de cocción. El gripper fue diseñado para adaptarse a diferentes tamaños de arepa, sujetarlas con firmeza sin dañarlas, y acoplarse correctamente al robot. Durante su fabricación y prueba se validó que cumplía con los requisitos funcionales del proceso.

La simulación completa del sistema fue desarrollada en RoboDK, donde se logró ejecutar todo el ciclo: selección de la arepa, traslado, posicionamiento en la parrilla y liberación. Sin embargo, en la implementación física solo se realizaron las trayectorias del robot, ya que por razones técnicas no se retiró el gripper neumático previamente instalado en el equipo del laboratorio. Aun así, las trayectorias programadas fueron verificadas como funcionales y seguras, demostrando que la solución es totalmente viable con el gripper diseñado por el equipo.

#### Proceso de alistamiento

El proceso simulado y programado sigue los siguientes pasos:

1. Se selecciona la arepa.
2. El robot se desplaza hacia la posición correspondiente en la vitrina de almacenamiento.
3. El gripper simulado toma la arepa y la traslada hacia la zona de cocción.
4. Se deposita la arepa en la matriz de cocción.

#### Herramientas y piezas utilizadas

- Robot Yaskawa
- Software de simulación RoboDK
- Gripper diseñado:
- Vitrina de almacenamiento.
- Arepa de prueba (cilindro recubierto con cinta negra).

### Diagrama de flujo de las acciones del robot con sus respectivas descripciones

```mermaid
flowchart TD
    A[Inicio: Conexión a RoboDK] --> B[Selección y validación del robot, gripper y frames]
    B --> C[Configuración inicial: herramienta, velocidad, blending, posición HOME]
    C --> D[Preparar entorno: validar frame y objeto Arepa1, configurar frame MESA]
    D --> E[Recoger arepa de la mesa]
    E --> F[Colocar arepa en la primera parrilla - Pan1]
    F --> G[Regresar, recoger de nuevo y rotar eje]
    G --> H[Colocar arepa en la segunda parrilla - Pan2]
    H --> I[Regreso a HOME y restablecer frame original]
    I --> J[Fin del proceso]
```

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
Para observar el modelo en software, se agrega una carpeta la cual contiene el proyecto. Se observa de la simulación que la estatería se ubicó de tal manera que el robot alcanzace una mesa disponible en el propio laboratorio. Ya si se quiere visualizar o descargar la simulación completa en el programa RoboDK, se puede hacer clic en la siguiente imagen que lo guiará a la carpeta la cual contiene el proyecto completo.

<p align="center">
  <a href="./PROYECTO">
    <img src="https://github.com/user-attachments/assets/6662a400-f384-46a8-977a-d9c809d1a4c0" alt="Gripper" width="650"/>
  </a>
</p>


### Código fuente comentado y discutido del módulo utilizado para el desarrollo del proyecto

```python
from robodk.robolink import *    # API para comunicarse con RoboDK
from robodk.robomath import *    # Funciones de álgebra y transformaciones
import math

#----------------------------------------------
# 1) Conexión a RoboDK e inicialización del robot
#----------------------------------------------

RDK = Robolink()

# Seleccionar un robot manualmente si hay más de uno en la estación
robot = RDK.ItemUserPick("Selecciona un robot", ITEM_TYPE_ROBOT)

# Cargar el gripper
gripper_name = "Gripper v7"
gripper = RDK.Item(gripper_name, ITEM_TYPE_TOOL)
if not gripper.Valid():
    raise Exception(f'No se encontró el gripper "{gripper_name}" en la estación.')

robot.setTool(gripper)

#----------------------------------------------
# 2) Configuración inicial: HOME y parámetros básicos
#----------------------------------------------

frame_name2 = "HOME"
frame2 = RDK.Item(frame_name2, ITEM_TYPE_FRAME)
if not frame2.Valid():
    raise Exception(f'No se encontró el Frame "{frame_name2}" en la estación.')

robot.setPoseFrame(frame2)
robot.setPoseTool(robot.PoseTool())
robot.setSpeed(300)   # Velocidad en mm/s
robot.setRounding(5)  # Blending en mm

robot.MoveL(transl(0, 0, 0))  # Moverse a posición base de HOME

#----------------------------------------------
# 3) Validar elementos necesarios para el proceso
#----------------------------------------------

# Frame y objeto de la arepa
frame_Arepa1 = "FrameArepa1"
frameArepa1 = RDK.Item(frame_Arepa1, ITEM_TYPE_FRAME)
if not frameArepa1.Valid():
    raise Exception(f'No se encontró el Frame "{frame_Arepa1}" en la estación.')

arepa = RDK.Item("Arepa1", ITEM_TYPE_OBJECT)
if not arepa.Valid():
    raise Exception('No se encontró el objeto "Arepa1" en la estación.')

# Frame de la mesa
frame_name = "MESA"
frame = RDK.Item(frame_name, ITEM_TYPE_FRAME)
if not frame.Valid():
    raise Exception(f'No se encontró el Frame "{frame_name}" en la estación.')

robot.setPoseFrame(frame)
robot.setPoseTool(robot.PoseTool())
robot.setSpeed(300)
robot.setRounding(5)

#----------------------------------------------
# 4) Recoger la arepa desde la mesa
#----------------------------------------------

robot.MoveL(transl(-100, 0, -50))       # Posicionarse sobre la mesa
robot.MoveL(transl(-100, 140, -50))     # Movimiento lateral
robot.MoveL(transl(70, 140, -50))       # Posicionarse cerca de la arepa
robot.MoveL(transl(70, 140, 0))         # Bajar al nivel de la arepa
arepa.setParent(gripper)               # Agarrar la arepa
robot.MoveL(transl(70, 140, -50))       # Levantar
robot.MoveL(transl(-100, 140, -50))     # Alejarse

#----------------------------------------------
# 5) Colocar la arepa en la primera parrilla
#----------------------------------------------

frame_Pan1 = "FramePan1"
framePan1 = RDK.Item(frame_Pan1, ITEM_TYPE_FRAME)
if not framePan1.Valid():
    raise Exception(f'No se encontró el Frame "{frame_Pan1}" en la estación.')

robot.setPoseFrame(framePan1)
robot.setPoseTool(robot.PoseTool())
robot.setSpeed(300)
robot.setRounding(5)

robot.MoveL(transl(-270, 0, -50))
robot.MoveL(transl(0, 0, -50))
robot.MoveL(transl(0, 0, 0))
arepa.setParent(framePan1)             # Soltar arepa en la primera parrilla
robot.MoveL(transl(0, 0, -50))
robot.MoveL(transl(-270, 0, -50))

#----------------------------------------------
# 6) Volver a HOME
#----------------------------------------------

frame2 = RDK.Item("HOME", ITEM_TYPE_FRAME)
robot.setPoseFrame(frame2)
robot.setPoseTool(robot.PoseTool())
robot.setSpeed(300)
robot.setRounding(5)
robot.MoveJ(transl(0, 0, 0))

#----------------------------------------------
# 7) Recoger la arepa nuevamente para rotarla
#----------------------------------------------

robot.setPoseFrame(framePan1)
robot.setPoseTool(robot.PoseTool())
robot.setSpeed(300)
robot.setRounding(5)

robot.MoveL(transl(-270, 0, -50))
robot.MoveL(transl(0, 0, -50))
robot.MoveL(transl(0, 0, 0))
arepa.setParent(gripper)
robot.MoveL(transl(0, 0, -200))

# Rotar el eje 6 del robot 180 grados
joints_actuales = robot.Joints().list()
joints_actuales[5] += 180
robot.MoveJ(joints_actuales)

#----------------------------------------------
# 8) Colocar la arepa en la segunda parrilla
#----------------------------------------------

frame_Pan2 = "FramePan2"
framePan2 = RDK.Item(frame_Pan2, ITEM_TYPE_FRAME)
if not framePan2.Valid():
    raise Exception(f'No se encontró el Frame "{frame_Pan2}" en la estación.')

robot.setPoseFrame(framePan2)
robot.setPoseTool(robot.PoseTool())
robot.setSpeed(300)
robot.setRounding(5)

robot.MoveL(transl(0, 0, 200))
robot.MoveL(transl(0, 0, 0))
arepa.setParent(framePan2)            # Soltar arepa en la segunda parrilla
robot.MoveL(transl(0, 0, 200))

#----------------------------------------------
# 9) Finalización: volver a HOME y restaurar frame
#----------------------------------------------

robot.setPoseFrame(frame2)
robot.setPoseTool(robot.PoseTool())
robot.setSpeed(300)
robot.setRounding(5)
robot.MoveJ(transl(0, 0, 0))

# Restaurar jerarquía de la arepa
arepa.setParent(frameArepa1)
```

### Comparación del tiempo de alistamiento manual y de operación automatizada para las combinaciones seleccionadas

Para evaluar la eficiencia de la solución automatizada frente al proceso tradicional manual, se realizó una comparación de tiempos tomando como referencia las etapas principales del alistamiento de las arepas: selección, agarre, desplazamiento y colocación sobre la parrilla de cocción.

| Actividad                                      | Proceso Manual (promedio) | Proceso Automatizado (simulación RoboDK) |
| ---------------------------------------------- | ------------------------- | ---------------------------------------- |
| **Alistamiento inicial del sistema**           | 5 s                       | 15 s                                     |
| Identificación y selección de la arepa         | 5 s                       | 1 s                                      |
| Toma del producto y desplazamiento             | 8 s                       | 5 s                                      |
| Colocación sobre la parrilla                   | 4 s                       | 2 s                                      |
| **Tiempo total por arepa (post-alistamiento)** | **17 s**                  | **8 s**                                  |

Análisis:
- Tiempo de alistamiento inicial: El sistema automatizado requiere una configuración previa más extensa (calibración, carga de programa, alineación del gripper, etc.), lo cual lo hace más lento en el arranque comparado con el proceso manual, que puede empezar casi de inmediato.

- Ciclo operativo (por cada arepa): Una vez en funcionamiento, el robot supera ampliamente al método manual. Ejecuta con mayor precisión y repetitividad las tareas programadas, disminuyendo a más de la mitad el tiempo por unidad.

- Eficiencia en cadena: Cuando se considera una producción continua o por lotes (por ejemplo, 10 o más arepas), el alistamiento inicial del robot se diluye en el total del proceso, y el sistema automatizado se vuelve claramente más rápido y eficiente.

Por ejemplo se tiene la realización de 10 arepas.

| Proceso      | Tiempo Total Estimado                     |
| ------------ | ----------------------------------------- |
| Manual       | 10 × 17 s = **170 s**                     |
| Automatizado | 15 s (alistamiento) + 10 × 8 s = **95 s** |

En conclusión, aunque el sistema automatizado tiene un alistamiento inicial más lento, su desempeño a escala lo hace mucho más eficiente que el proceso manual. Esto demuestra que para procesos repetitivos y de producción en cadena, la automatización no solo reduce el tiempo operativo, sino que también mejora la precisión, higiene y estandarización del producto final.

### Vídeo tipo presentación con duración entre 10 a 15 minutos
Debería incluir el clip de introducción de LabSIR, seguido de un banner de la Universidad Nacional de Colombia, autores, profesores, curso, año,
etc. Intro LabSIR, el vídeo debe incluir:
- La simulación en en el software predeterminado con líneas de trazado de trayectorias y cálculo del tiempo total de ensamble. Se debe incluir a la simulación los modelos geométricos de la vitrina, espacio de cocción y arepas.
- Vídeo de implementación del proyecto donde todos los integrantes del grupo participen y expliquen la solución planteada
[![Watch the video](https://img.youtube.com/vi/pZ8izMtvlJU/maxresdefault.jpg)](https://youtu.be/pZ8izMtvlJU)
https://youtu.be/pZ8izMtvlJU
