# Tips-Clean-code-Robert-Martin-Book-spanish
 *Estaré mejorando poco a poco según avance la lectura, bienvenido las colaboraciones*
## Tabla de Contenido
  1. [Nombres, Functiones, comentarios](#nombres-functiones-comentarios)
  1. [Formato](#formato)

## Nombres, Functiones, comentarios
-el nombre de una clase no puede ser un verbo  solo los funciones
- la primera de la funciones es que sea reducido y la segunda que sea mas reducido
-las funciones solo deben hacer una cosa
- si una funcion se puede divir a mas secciones es evidente que no hace solo una cosa
- el codigo debe leerse de arriba a abajo
-usar nombres descriptivos
- el n numero idial de argumentos de una funcion es  cero
-pasar un booleano a una funcion no es buena practica, porque obliga hacer mas de una cosa a la funcion
-forma de reducir argumentos es objeto como argumento
- es mejor devolver exepciones que codigo de error
- si incluye una funcion try debe ser la primera linea- la funcion solo hace eso (solo procesa error) (extrer el cuerpo de try catch
- no repitirse (el principio DRY)
-los programadores ecperimentados piensan en los siste,as como en historias a contar,
-no comente el codigo incorrecto reescribalo
- los comentarios pueden resultar dando mala informacion con el tiempo cuando cuando el codigo
- no es bueno tener codigo comentado se acumulan con el tiempo
- no usar comentatios si se puede usar una funcion o una variable
-no es bueno tener codigo comentado
- el javadoc es olo para API publicas

Formato
- recomendable cada archivo de java tenga entre 100 a 500 lineas de codigo en promedio, files de tamalño pequeño son mas entendibles
- es importante separacion entre funciones con un espacio (la densidad vertical)
- los conceptos relacionados entre si deben mantener juntos verticalmente
-orden vertical,dependencia de invocaciones hacia abajo
-limite de caracteres horizontal es de 120

Objetos y estructura de datos
- no mostrar los detalles de los datos, sino expresarlos en terminos abstractos.
- la ley de demiter   (125)los objetos ocultan datos y muestran operaciones  Ley de Demeter: “Habla solo con tus amigos cercanos. No hables con extraños.”
Una de las principales cosas que la Ley de Demeter quiere evitar que hagas es esto:
objetoA.metodoDeA().metodoDeB().metodoDeC();

Procesar errores
Usar exepciones en lugar de cogigos devueltos
- crear primero la instruccion try-catch- finally-- recomendableusar TDD para generear exepciones
-usar excepciones sin comprobar
- la excepciones comprobadas rompem la encapsulacion, es util cuando tienes crear una biblioteca util, sino el coste de dependencia crece mucho
- definir clases de excepcion de acuerdo a las necesidades del invocador
- mo devolver null
- no pasar null


Límetes o frenteras.

integrar codigo externo con nuestro
- Con los APIS realizar experimentos controlados para ver si entendemos, 
. También permiten comprobar que las nuevas versiones de la librería siguen cumpliendo con nuestras necesidades.
-
Test unitarios
los test se crean unos segundo antes que el codigo real
-las pruebas cambian de acuerdo a la evolucion del codigo
-elcodigo de prueba es tan importante como el de la porcucion
- las pruebas deben ser limpis..legibilidad, claridad, simplicidad y densidad de expresion
-usar en los test el patron  generar-operar y comprobar
- recomendable una afirmacion por prueba  recomendable usar la comvencion dado- cuando-entonces
-un solo concepto por prueba
- seguir la regla FIRST,, rapidez,independencia,repeticion,validacion automatica y puntualidad


Clases
una clase debe comensar con la lista de variable,constantes publicass, c privvadas, variables de instancia luego funciones
las clases deben ser de tamaño reducido: el tamaño es su responsabilidades y por eso nombre de la clase debe describir responsabilidades que desempeña




168
