# Laboratorio #1 Robótica 
Primer laboratorio de la asignatura de Robótica de la Universidad Nacional de Colombia 2023-i. En esta práctica se busca usar el manipulador para escribir la secuencia "TNF" en un tablero.

<p align="center">
<img marigin="auto" src="https://github.com/mora200217/labrob-1/blob/master/assets/funcional.gif" width="60%"/> 
</p>

**Integrantes**: 
* Nelson David Ramírez Marín
* Andrés Zuleta 
* Andrés Morales Martínez 

## Planteamiento del Problema 
Se requiere usar el sistema robotizado del manipulador de *ABB IRB 140* para poder escribir una secuencia de letras en diversas superficies de tablero. El problema se divide en tres (3) fases: Diseño de la herramienta, Definición de Trayectorias en RobotStudio y ejecución del programa de RAPID en el manipulador. 

## Diseño 
La herramienta tiene como objetivo el servir como soporte para un marcador de tablero, para que el manipulador pueda escribir. Debido a que nuestra prioridad era la estabilidad del marcador durante el proceso de escritura, se optó por una ensamble de dos piezas. 

<p align="center">
<img margin="auto" src="https://github.com/mora200217/labrob-1/blob/master/design/sketch.jpeg" width="60%"/> 
</p> 


### Base del Ensamble
La base, consistente con las dimensiones de la hoja de datos suminsitrado por ABB, fue diseñada con dos particularidades: 

- Una extrusión de alineación para el plato. 
- Un cilindro de acople para la base del marcador. Similar a las terminaciones de las tapas plásticas. 

### Soporte Cilindrico
Se optó por esta pieza para encerrar el marcador y garantizar un mejor acople. Tiene un cono interno para evitar desplazamiento radial externo del marcador, y en los laterlaes del soporte se agregaron tornillos para fijar aún más el marcador. 


<p align="center">
<img margin="auto" src="https://github.com/mora200217/labrob-1/blob/master/assets/sim-impresion.jpeg" width="20%"/> 
<img margin="auto" src="https://github.com/mora200217/labrob-1/blob/master/assets/impresion.jpeg" width="20%"/> 
<img margin="auto" src="https://github.com/mora200217/labrob-1/blob/master/assets/resultado.jpeg" width="20%"/> 

</p> 




## Código en RAPID 
Desde RobotStudio, se construyó la trayectoria en 3 fases: Ubicar un punto Home, escribir una letra y subir a un punto "muerto" para reajustar posición y vontinuar con la siguiente letra. Se cargó el modelo 3D de la herramienta para tener un nuevo "Tool" en RobotStudio, para redefinir el TCP (la punta del marcador) para el proceso. 

<p align="center">
<img margin="auto" src="https://github.com/mora200217/labrob-1/blob/master/assets/robotstudio.jpeg" width="60%"/> 

</p> 



## Ejecución
Se exportaron las rutinas desde RobotStudio para tener el RAPID que cargar al controlador desde el FlexPendant. Se realizó una etapa de prueba, subiendo la coordenada vertical (z) del workobject utilizado, para hacer la revisión de cumplimiento de rutina. Finalmente, se ajusta iterativamente el eje vertical, buscando que workobject coincida con la superficie a escribir, y comenzar con el proceso de escritura de las 3 letras cargadas. 

**Video Trayectoria 1:** https://youtu.be/atYaf5iX8Yo

**Video Trayectoria 2:** https://youtu.be/zLNep-NyKM0 

## Conclusiones 

1. Es muy importante tener claro los marcos de referencia tanto de la herramienta como de los puntos que se crean para que sean concordantes los movimientos y trayectorias que se desean.
2. El buen diseño CAD de una herramienta puede facilitar mucho todo el proceso de calibracion que se debe hacer en un manipulador industrial.
3. Es muy importante tener un resorte en la herramienta para que cualquier proceso de escritura sea mas facil de desarrollar.
