# Tips-Clean-code-Robert-Martin-Book-spanish
 *Estaré mejorando poco a poco según avance la lectura, bienvenido las colaboraciones*
## Tabla de Contenido
  1. [Nombres, Funciones, Comentarios](#nombres-funciones-comentarios)
  1. [Formato](#formato)
  1. [Objetos y Estructura de Datos](#objetos-estructura-datos)
  1. [Procesar Errores](#procesar-errores)
  1. [Límites o Fronteras](#limites-fronteras)
  1. [Test Unitarios](#test-unitarios)
  1. [Clases](#clases)


## Nombres, Funciones, comentarios
  - El nombre de una clase no puede ser un verbo  solo las funciones. 
  - La primera regla de las funciones es que sea reducido y la segunda que sea mas reducido.
  - Las funciones solo deben hacer una cosa.
  - Si una función se puede dividir a más secciones es evidente que no hace solo una cosa.
  - El código debe leerse de arriba a abajo.
  - Usar nombres descriptivos para las funciones.
  - El número ideal de argumentos de una función es  cero.
  - Pasar un booleano a una función no es buena práctica, porque obliga hacer mas de una cosa a la función.
  - Una forma de reducir argumentos es pasar objeto como argumento.
  - Es mejor devolver excepciones que código de error.
  - Es importantes usar el principio DRY (No repetir).
  - Los programadores experimentados piensan en los sistemas como en historias a contar.
  - No comente el código incorrecto rescríbalo.
  - Los comentarios pueden resultar dando mala información con el tiempo, porque se acumulan con el tiempo.
  - No usar comentarios si se puede usar una función o una variable descriptivo.
  - Es recomendable usar javadoc, solo cuando desarrollas APIs públicas.
  
## Formato
  - Recomendable que cada archivo de java tenga entre 100 a 500 líneas de código en promedio, archivos de tamaño pequeño son más entendibles.
  - Es importante la separación entre funciones con un espacio (la densidad vertical).
  - Los conceptos relacionados entre si deben mantenerse juntos verticalmente.
  - Orden vertical, dependencia de invocaciones hacia abajo.
  - Límite de caracteres horizontal en promedio debería ser de 120.

## Objetos y Estructura de Datos
  - No mostrar los detalles de los datos, sino expresarlos en términos  abstractos.
  - Los objetos ocultan datos y muestran operaciones  Ley de Demeter: "Habla solo con tus amigos cercanos. No hables con extraños" y 
  - Una de las principales cosas que la Ley de Demeter quiere evitar que hagas es esto:
  
  ```java
  objetoA.metodoDeA().metodoDeB().metodoDeC();
  ```
  
## Procesar Errores
  - Usar excepciones  en lugar de cogidos devueltos.
  - Crear primero la instrucción try-catch-finally,recomendable usar TDD para generar excepciones.
  - Usar excepciones no comprobadas.
  - La excepciones comprobadas rompen la encapsulación, es útil cuando tienes crear una libreria, sino el coste de dependencia crece mucho.
  - Definir clases de excepción de acuerdo a las necesidades del invocador.
  - No devolver null tampoco pasar null.

## Límites o Fronteras
  *Integrar código externo con nuestro*
  - Con los APIS recomendable realizar experimentos controlados para ver si entendemos, También permiten comprobar que las nuevas versiones de la librería siguen cumpliendo con nuestras necesidades.

## Test Unitarios
  - Los test se crean antes que el código real
  - Las pruebas cambian de acuerdo a la evolución del código
  - El código de prueba es tan importante como el de la producción
  - Las pruebas deben ser limpias:legibilidad, claridad, simplicidad y densidad de expresión
  - Usar en los test el patrón  generar-operar y comprobar
  - Recomendable una afirmación por prueba  recomendable usar la convención dado-cuando-entonces
  - Un solo concepto por prueba
  - Seguir la regla FIRST, rapidez, independencia, repetición, validación automática y puntualidad

## Clases
  - Una clase debe comenzar con la lista de variable , constantes publicas, privadas, variables de instancia luego funciones
  - Las clases deben ser de tamaño reducido: el tamaño es depende de las responsabilidades y por eso nombre de la clase debe describir responsabilidades que desempeña


pag.168

