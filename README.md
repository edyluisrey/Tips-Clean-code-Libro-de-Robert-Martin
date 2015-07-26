# Tips-Clean-code-libro-de-Robert-Martin
 *Estaré mejorando poco a poco según avance la lectura, bienvenido las colaboraciones*
## Tabla de Contenido
  1. [Nombres, Funciones, Comentarios](#nombres-funciones-comentarios)
  1. [Formato](#formato)
  1. [Objetos y Estructura de Datos](#objetos-estructura-datos)
  1. [Procesar Errores](#procesar-errores)
  1. [Límites o Fronteras](#limites-fronteras)
  1. [Test Unitarios](#test-unitarios)
  1. [Clases](#clases)
  1. [Sistemas](#sistemas)
  1. [Emergencia](#emergencia)
  1. [Concurrencia](#concurrencia)


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
  - Las clases dolo deben tener una responsabilidad (principio de resonsabilidad unica).
  - Las clases deben tener un número reducido de variables de instancia.
  - Las clases son más consistente, mientras la cohesion de nuestras clases sea elevada (si las variable se usa en cada metodo es maxima la cohesion)
  - La division de grandes funciones en mas pequeñas aumenta la proliferación de clases y eso es bueno (las clases se vuelven mas consistentes)
  - Organizar los cambios con el principio abierto cerrado de OOP (las clases deben ser abierto para extender y cerrado para modificar)
  - Es recomendable recurrir a interfaces y clases abstractas para aislarnos de los cambios.
  - Nuestras clases deben depender de abstracciones, no de detalles concretos (DIP principio de inversions de dependencias)

## Sistemas  
  - El sistema software debe separar el proceso de inicio, en el que se crean los objetos de la aplicación y se conectan las dependencias, de la logica de ejecución.
  - Una forma de separar la construcción del uso consiste en trasladar todos los aspectos de la constrccion al Main.
  - Un mecanisco para separar la construcción del uso es la inyección de dependencias.
  - Conseguir sistemas perfectos a la primera es un mito, por el contrario, debemos implementar hoy, y refactorizar y ampliar mañana, es la esencia de la agilidad. El desarrollo con test, la refactorización y el código limpio que se genera hace que funcione a  nivel de codigo.

## Emergencia
 - Un diseño es sencillo si cumple las siguientes 4 reglas: ejecuta todas las reglas, no contiene duplicados, expresa la intención del programador y  minimiza el número de clases y métodos.
 - Los duplicados son los mayores enemigos de un sistema bien diseñado
 - El patrón método de plantillas es una técnica muy usada para eliminar duplicados de nivel superior
 - El código debe expresar con mas claridad la intención de su autor (reduce el coste de mantenimiento)
 - Puede expresarse  eligiendo nombres adecuados, responsabilidades adecuadas usar patrones y estándares

## Concurrencia
 - La concurrencia es una estrategia de desvinculación. Nos permite desvincular lo que se hace de dónde se hace
 - La aplicación parece una serie de equipos colaboradores y no un gran bucle principal, esto puede hacer que el sistema sea más facil de comprender 
 - El diseño cambia al crear programas concurrentes que la de un sistema de un solo proceso
 - Es importante aplicar principo de responsabilidad única.
 - Es recomendable separar el código de concurrencia del resto del codigo
 - Es recomendable encapsualar los datos y limitar el acceso a los datos compartidos

pag..211


