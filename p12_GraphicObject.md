# PRIVATE







# Práctica 12. Programación Gráfica y Orientada a Eventos. HTML. Canvas. Movimiento y control de un objeto
# gráfico
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

### Movimiento y control de un objeto gráfico

Desarrolle un programa `bola_movil.js` que muestre en pantalla una ventana
rectangular con fondo de color azul sobre la que se verá un círculo centrado en la ventana
y un panel con cuatro botones que permiten mover el círculo hacia arriba, abajo, izquierda
y derecha.


%%%%%%%%%%%%%%%%%%%% Fig. %%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
\begin{figure}[h]
\centerline{\includegraphics[width=0.5\linewidth]{bola}}
\caption{Interfaz gráfica del programa} 
\label{fig:bola} 
\end{figure}
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
La Figura \ref{fig:bola} muestra un ejemplo al que debería parecerse la salida del programa a elaborar.


Las siguientes deben tomarse como especificaciones de la aplicación a desarrollar:
\begin{itemize}
\item Utilizando \texttt{AssertJ}, desarrolle tests unitarios que aseguren que el comportamiento del progama
      es el deseado.
\item Utilice también \texttt{JaCoCo} para analizar el cubrimiento que los tests unitarios realizan sobre el
      código desarrollado.
\item La interfaz contendrá los cuatro botones: \texttt{Arriba}, \texttt{Abajo}, \texttt{Izquierda}, \texttt{Derecha}
      cuyas funciones ya se han comentado.
\item Cuando el círculo alcanza cualquiera de los bordes de la ventana, se ha de impedir
      su movimiento en la dirección del borde alcanzado (los bordes son impenetrables).
\item El número de pixeles que se desplaza el círculo por la ventana con cada pulsación de un botón
      será un parámetro que el programa ha de leer en línea de comandos.
\item Si el programa se ejecuta sin pasar ningún parámetro en línea de comandos, se debe escribir
      un mensaje en la consola indicando la forma correcta de ejecución del programa.
\item Se valorará positivamente que el diseño sea efectivamente orientado a objetos, modelando con diferentes
      clases los distintos elementos que intervienen en la aplicación.
\item El programa que aquí se propone se tomará como punto de partida para desarrollar una aplicación similar
      a la que aquí se propone. 
      Así pues, será beneficioso el realizar un diseño muy modular y flexible.
\item Evite utilizar clases o métodos que no hayan sido explicados en las clases de teoría.
\end{itemize}
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%

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
* [ESLint](https://eslint.org/)
* [JSDoc](https://jsdoc.app/)
* [The Modern Javascript Tutorial](https://javascript.info)
* [PAI Code Examples](https://github.com/ULL-ESIT-PAI-2021-2022/PAI-class-code-examples/tree/master/src)
* [Google JavaScript Style Guide](https://google.github.io/styleguide/jsguide.html)
