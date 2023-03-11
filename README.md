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

<img marigin="auto" src="https://github.com/mora200217/labrob-1/blob/master/assets/resultado.jpeg" width="20%"/> 

### Base del Ensamble
La base, consistente con las dimensiones de la hoja de datos suminsitrado por ABB, fue diseñada con dos particularidades: 

- Una extrusión de alineación para el plato. 
- Un cilindro de acople para la base del marcador. Similar a las terminaciones de las tapas plásticas. 

### Soporte Cilindrico
Se optó por esta pieza para encerrar el marcador y garantizar un mejor acople. Tiene un cono interno para evitar desplazamiento radial externo del marcador, y en los laterlaes del soporte se agregaron tornillos para fijar aún más el marcador. 

## Código en RAPID 


## Conclusiones 

1. Es muy importante tener claro los marcos de referencia tanto de la herramienta como de los puntos que se crean para que sean concordantes los movimientos y trayectorias que se desean.
2. El buen diseño CAD de una herramienta puede facilitar mucho todo el proceso de calibracion que se debe hacer en un manipulador industrial.
3. Es muy importante tener un resorte en la herramienta para que cualquier proceso de escritura sea mas facil de implementar.
