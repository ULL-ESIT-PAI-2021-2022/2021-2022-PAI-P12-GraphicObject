# PRIVATE







# Práctica 12. Programación Gráfica y Orientada a Eventos. HTML. Canvas. Ajedrez.
### Factor de ponderación: 10

### Objetivos
Los objetivos de esta tarea son poner en práctica:
* Conceptos de Programación orientada a eventos en JavaScript.
* Conceptos de Programación Gráfica en JavaScript usando la API Canvas.
* Metodologías y conceptos de Programación Orientada a Objetos en JavaScript.
* Principios y Buenas prácticas de programación Orientada a Objetos.
* El uso de elementos HTML básicos.
* El uso de algunas propiedades básicas de CSS para dotar de estilo a una página web simple.

### Rúbrica de evaluacion del ejercicio
Se señalan a continuación los aspectos más relevantes (la lista no es exhaustiva)
que se tendrán en cuenta a la hora de evaluar esta práctica:
* Se valorará la realización de las diferentes tareas que se proponen.
* El comportamiento del programa debe ajustarse a lo solicitado en este documento.
* Capacidad de la programadora de introducir cambios en el programa desarrollado.
* Conocer y poner en prácticas los principios y buenas prácticas de programación orientada a objetos.
* El programa debe ajustarse al paradigma de Orientación a Objetos.
* Deben usarse estructuras de datos adecuadas para representar los diferentes elementos que intervienen en el problema
* Acreditar que se sabe generar informes de cubrimiento de código utilizando tanto 
[Jest](https://jestjs.io/)
como
[CodeCov](https://docs.codecov.com/docs)
* Saber corregir bugs en sus programas utilizando el depurador de Visual Studio Code
* Ser capaz de desarrollar tests unitarios para sus programas utilizando 
[Jest](https://jestjs.io/)
* Acreditar que sabe depurar sus programas usando Visual Studio Code.
* Acreditar su capacidad para configurar y utilizar 
[ESLint](https://eslint.org/)
  y que es capaz de trabajar con la misma en Visual Studio Code.
* El código ha de estar documentado con 
[JSDoc](https://jsdoc.app/). 
  y ha de acreditarse la capacidad de generar documentación para sus programas utilizando la herramienta.
  Haga que la documentación del programa generada con JSDoc esté disponible a través de una web alojada en su máquina IaaS de la asignatura.
* Se comprobará que el código que el alumnado escribe se adhiere a las reglas de la 
[Guía de Estilo de Google para Javascript](https://google.github.io/styleguide/jsguide.html).
* Todas las prácticas realizadas hasta la fecha, incluída la que se presenta para su evaluación, se encuentran alojadas en repositorios privados de GitHub.
* Acreditar que es capaz de editar ficheros de forma remota en su VM usando Visual Studio
  Code (VSC)

### Indicaciones de caracter general
Previo a la implementación de cada clase, diseñe y desarrolle un conjunto de tests para probar el correcto
funcionamiento de todos los métodos públicos.

Encapsule las clases en módulos que exporten la correspondiete clase hacia otros programas clientes que pudieran utilizarla.

Configure para la práctica una página web que sirva de índice para mostrar la documentación generada por
JSDoc para todos los ejercicios de la práctica.

Todo el código estará ubicado en el directorio `src` del proyecto. Use subdirectorios de éste si le resulta conveniente.

Configure un fichero `package.json` en el directorio raíz de su repositorio de modo que ejecutando 
`npm install` queden instaladas todas las dependencias de su proyecto.

### El problema de las reinas que se atacan
En esta práctica se realizarán ejercicios relacionados con el juego del Ajedrez.
Consulte
[Wikipedia](https://es.wikipedia.org/wiki/Ajedrez)
para un conocimiento básico del juego, en caso de que no lo conozca.

Comience por resolver el problema 
[Queen Attack](https://exercism.org/tracks/typescript/exercises/queen-attack)
del *track* de Typescript de Exercism.
El problema ya lo debiera tener resuelto en Javascript, de modo que pasarlo a TS no debiera entrañar mayor
dificultad y le servirá para conocer lo que añade TS a JS en cuanto a la sintaxis de clases.

Si revisa los tests del ejercicio observará que la solución requiere que cree una clase `QueenAttack`
cuyo constructor toma como parámetros las posiciones de un par de reinas de la forma:

`const queens = new QueenAttack({ white: [2, 4], black: [6, 6] });`

### El problema de las 8 reinas
El problema de las 
[8 reinas](https://en.wikipedia.org/wiki/Eight_queens_puzzle) 
es un pasatiempo famoso consistente en colocar ocho reinas en un tablero de ajedrez de modo que no se amenacen.

Por ejemplo, esta solución:

```
0 1 2 3 4 5 6 7
Q . . . . . . . 0
. . Q . . . . . 1
. . . . Q . . . 2
...
...
```
es válida como solución del problema puesto que las reinas no se amenazan.

Comience por desarrollar un programa orientado a objetos sin programación gráfica `8queens1.js` que resuelva 
el problema de las 8 reinas: el programa ha de hallar una configuración que posicione 8 reinas en un tablero de ajedrez de modo que no se amenacen entre sí
y las soluciones han de escribirse en consola de modo similar al ejemplo previo.

### La clase *Chess*
Se propone tomar como punto de partida el programa que resuelve el problema de
las 8 reinas para añadirle una interfaz gráfica basada en HTML y CSS y poder ejecutar el programa a través de esa interfaz web.

Se propone desarrollar una clase `Chess` 
que posibilite la visualización en una página web de un tablero de ajedrez con sus figuras.
La clase ha de encapsularse en un módulo ES6 `chess.js`.

Tenga en cuenta las siguientes especificaciones a la hora de diseñar su programa:

* Comience por adaptar su programa del problema de las 8 reinas para dotarlo de capacidades gráficas.

* Desarrolle una página web cuya interfaz gráfica se asemeje lo más posible, en cuanto a su apariencia, no en
  cuanto a sus funcionalidades, a la que se muestra en esta imagen:
![Ajedrez](https://raw.githubusercontent.com/fsande/PAI-Labs-Public-Data/master/img/p11_Chess/chess.png "Ajedrez")
  También puede ver la interfaz que se pretende imitar iniciando una partida en 
  [esta página de juego on-line de ajedrez](https://lichess.org).
	Su página ha de imitar colores, tipografías, tamaños y distribución de los elementos.
  En el directorio `img` de este proyecto puede Ud. encontrar imágenes gráficas para las figuras del juego.
  Puede Ud. usar estas u otras si le parecen más adecuadas.

* Se colocarán en la página enlaces similares a los que figuran en la página de referencia, pero en su caso
	esos enlaces no estarán operativos (no enlazan a otras páginas) o en todo caso enlazarán con páginas
  alojadas en su máquina IaaS de la asignatura.

* Añada un pie de página (*footer*) en el que incluya información sobre la Universidad,
  titulación y asignatura.

* Añada en su página los siguientes elementos:

1. Un botón `Generar solución` que al ser pulsado dibuje en el tablero sucesivas soluciones al problema de las 8
reinas mostrando una solución en pantalla durante 1 segundo antes de pasar a la siguiente.

2. Un segundo botón `Partida de ajedrez` que al ser pulsado dibuje en el tablero la configuración inicial de
las piezas de una partida de ajedrez. 

* Sustituya en su página el panel que figura a la derecha del tablero en la web de referencia e incluya en él
  un panel en el que, para cada solución que se muestre para el problema de las 8 reinas imprima 
	en [notación algebraica](https://en.wikipedia.org/wiki/Algebraic_notation_(chess)) las posiciones que ocupa
	cada una de las 8 reinas ubicadas en el tablero.
	
* No añada a la interfaz gráfica (web) de su programa otros elementos que los que se describen en esta especificación.
  Trate asimismo de ceñirse a la utilización de los elementos HTML y CSS estudiados en las clases de teoría.

### Presentación de resultados
La visualización de la ejecución del programa se realizará a través de una página web alojada
en la máquina IaaS-ULL de la asignatura y cuya URL tendrá la forma:

`http://10.6.129.123:8080/einstein-albert-chess.html` [1]

en la que se incustará un canvas para dibujar el tablero.
Sustituya *Albert Einstein* por su nombre y apellido en la URL de su página.

Utilice código HTML y CSS para imitar en la medida de lo posible la apariencia de la web de referencia
[web de referencia](https://lichess.org/).

Diseñe asimismo otra página HTML simple 

`http://10.6.129.123:8080/index.html` [2]

que sirva de "página índice" para los ejercicios de la sesión de evaluación de la práctica.
La página [1] será uno de los enlaces de [2] y a su vez [1] tendrá un enlace "Home" que apunte a [2].
Enlace también en la página índice [2] las páginas que contienen los informes de documentación y de
cubrimiento de código de su proyecto.

## Referencias
* [8 reinas](https://en.wikipedia.org/wiki/Eight_queens_puzzle) El problema de las 8 reinas.
* [ESLint](https://eslint.org/)
* [JSDoc](https://jsdoc.app/)
* [The Modern Javascript Tutorial](https://javascript.info)
* [PAI Code Examples](https://github.com/ULL-ESIT-PAI-2021-2022/PAI-class-code-examples/tree/master/src)
* [Google JavaScript Style Guide](https://google.github.io/styleguide/jsguide.html)
