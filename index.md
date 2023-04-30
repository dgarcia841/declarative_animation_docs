# Animaciones declarativas
Esta herramienta le permite crear videos animados a partir de 
declaraciones por texto, contenidas dentro de documentos web.
Este documento presenta una guía general que explica cómo
utilizar la herramienta.

Desarrollado y escrito por Daniel García.

![Demostration 1](https://raw.githubusercontent.com/dgarcia841/declarative_animation_docs/main/demostration-1.gif)

## Enlaces
- Lea la referencia del lenguaje en [este enlace](https://dgarcia841.github.io/declarative_animation_docs/api/index.html).

- Lea la documentación del modelo matemático en [este enlace](https://dgarcia841.github.io/declarative_animation_docs/model/index.html).

## Introducción
A partir de los requerimientos establecidos para el proyecto, 
se ha definido una estructura del lenguaje de comandos que se 
describirá a continuación, a partir de un caso de ejemplo:

```anim
polygon:
origin = 1, 1
radius = 2
style = fill
background_opacity = 1/2
background = from red to blue in 4
sides = from 3 to 8 in 4
```

En lenguaje natural, esta porción de código declara un polígono
regular, le asigna una opacidad y color de fondo que cambia de
rojo a azul, y una cantidad de lados que cambia de 3 a 8, en un
tiempo de 4 segundos.

De manera general, la estructura del lenguaje se explica a
continuación:

-	Una nueva figura se declara escribiendo su nombre seguido del 
símbolo de dos puntos (`:`). La lista completa de figuras soportadas 
se encuentra la documentación, todos los nombres están en inglés.

-	Tras la declaración de una figura, se configuran sus propiedades. 
Cada figura cuenta con su propio conjunto de propiedades 
predeterminadas. Las propiedades se identifican con un nombre 
seguido de un signo de igual (`=`).

-	Tras el signo igual de una propiedad, se declara su valor o 
valores según requiera la propiedad.

-	Algunas propiedades se pueden configurar utilizando comandos, 
piezas más pequeñas dentro de la misma propiedad. Los comandos 
se identifican simplemente por su nombre, seguido del valor o 
los valores según requiera. En el ejemplo de arriba, las 
palabras `fill`, `from` y `to` son comandos.

Puede encontrar la lista completa de figuras, propiedades y
comandos en la documentación.


## Expresiones matemáticas
El valor de una propiedad o comando puede contener expresiones 
matemáticas, con soporte para aritmética básica y evaluación de 
funciones. Por ejemplo, una expresión válida que podría 
utilizarse como valor de una propiedad es:

```anim
circle:
radius = 1 + sqrt(pi)/2
```

En este ejemplo, el valor para el radio de un círculo se define 
con una operación matemática que involucra sumas, divisiones, la 
función raíz cuadrada y la constante matemática $\pi$.

Las operaciones aritméticas soportadas por el lenguaje dentro de 
una expresión matemática son: suma (+), resta (-), multiplicación 
(*), división (/), potenciación (^) y módulo (%). Un listado 
exhaustivo de las funciones y constantes soportadas por el 
lenguaje se encuentra la documentación.

## Uso de comandos
La mayoría de las propiedades de una figura se puede animar 
declarando diferentes estados. Para ello, los principales 
comandos que se utilizan son `from` (valor inicial), `to` 
(valor final) e `in` (tiempo de transición), como se ilustra 
a continuación:

```anim
circle:
radius = from 3 to 2 in 4
```

En lenguaje natural, el código anterior indica que el radio
del círculo pasará de 3 unidades a 2 unidades, en un tiempo 
de 4 segundos.

Nuevamente, el valor frente a cada comando puede incluir 
expresiones u operaciones matemáticas. El valor del tiempo 
siempre se mide en segundos. Asimismo, debe considerarse 
que en algunas propiedades deben definirse dos valores, 
por ejemplo, la posición de una figura; los comandos `from`
y `to` reciben igualmente dos valores en estos casos.
La posición de origen de una figura es un ejemplo de ello:

```anim
circle:
origin = from 1, 1 to 2, -1 in 3
```

Es posible declarar estados compuestos escribiendo secuencias 
de estos tres comandos consecutivamente, siempre teniendo en 
cuenta que lo que marca la declaración de un estado es el 
comando `in`. Por ejemplo, en la siguiente porción de código, 
se declara un círculo que se mueve entre los puntos $(1,1)$, 
$(2,2)$, $(2,-1)$ y $(1,-2)$, cada transición en un tiempo 
de un segundo:

```anim
circle:
origin = 
  from 1, 1  to 2, 2 in 1
    to 2, -1 in 1
    to 1, -2 in 1 
```

Nótese que, en la porción de código anterior, los comandos se 
separaron con saltos de línea. En general, el lenguaje es 
insensible a este tipo de separaciones, de modo que existe una 
libertad para organizar el código como se prefiera. Tampoco se 
necesita separar con saltos de línea las diferentes propiedades 
de la figura, éstas se identifican automáticamente cuando 
preceden un signo igual (=).

Existen otros comandos que se pueden declarar junto con los 
estados para realizar más configuraciones sobre la animación, 
como el comando reverse para invertir la animación una vez 
finalice, o el comando `restart` para que, por el contrario, 
esta se reinicie. Puede encontrar una lista exhaustiva de 
estos comandos en la documentación de cada figura.

## Comentarios
En ocasiones, puede llegar a ser útil añadir descripciones o 
anotaciones adicionales sobre el propio código de la animación
para mantener una idea clara de lo que se está graficando. 
Con esto en mente, se ha diseñado un sistema de comentarios 
simple para el lenguaje, de la siguiente manera:

```anim
polygon: // esto es un polígono
origin = 1, 1 // se dibuja en el punto (1,1)
radius = 2 // y otro comentario
```

Los comentarios se crean con dos barras inclinadas (//) a la 
izquierda, y van hasta el final de la línea de texto en la 
que se encuentren. Todo lo que esté marcado como comentario 
será ignorado completamente por el sistema, por lo que 
cualquier mensaje o texto que se escriba en uno será válido 
y no generará errores.

De manera similar, los comentarios también se pueden crear 
para ocupar varias líneas del texto y evitar el uso excesivo 
de barras inclinadas al inicio de cada línea. Este tipo de 
comentarios se denomina comentario multilínea, y se crea de 
la siguiente manera:

```anim
polygon: // esto es un polígono
/*
A continuación, una descripción más detallada
de la animación utilizando comentarios multilínea
*/
origin = 1, 1 // se dibuja en el punto (1,1)
radius = 2 // y otro comentario
```

Como se puede apreciar, el comentario multilínea inicia con 
una barra inclinada seguida de un asterisco (/\*), y finaliza 
con un asterisco seguido de una barra inclinada (*/) o, en su 
defecto, el final del texto. De la misma forma que los 
comentarios de una sola línea, los comentarios multilínea 
no son analizados por el sistema y se puede ingresar cualquier 
texto o mensaje en ellos.


## Secuencias
Cuando sea necesario crear múltiples figuras, en lugar de una sola, 
que siguen una secuencia determinada, es posible utilizar 
funcionalidad del lenguaje diseñada específicamente para ello. 
Las secuencias permiten repetir la declaración de una figura una 
cantidad determinada de veces, y siguen la siguiente sintaxis:

```txt
<figura> repeat <variable> <valor>:
<propiedad 1> = <valor> …
```

Nótese que la palabra clave `repeat` es necesaria después del nombre 
de la figura para identificar que se trata de una secuencia. 
En este caso, dicha palabra no se trata de un comando, pues no 
está acompañando ninguna propiedad sino la declaración de la 
propia figura.

En la posición de `<variable>`, se establece el nombre de una 
variable que actuará como subíndice de la secuencia, desde 0 
hasta el valor definido por `<valor>` (exclusivo). En <valor> es 
igualmente posible utilizar expresiones matemáticas, con el 
soporte ya mencionado para operaciones aritméticas y funciones.

A continuación, una porción de código que ejemplifica el 
funcionamiento de las secuencias:

```anim
circle repeat n 5:
origin = 0, -3 + n
radius = n/4
```

Mediante esta secuencia, se declaran 5 círculos usando la variable 
n como subíndice y, con ayuda de dicha variable, se declaran 
la posición y radio de cada círculo en la secuencia.

Usando las propiedades `start` y `end` que poseen todas las figuras, 
también es posible usar el subíndice de la secuencia para 
controlar el momento en el que una figura aparece en escena, 
por ejemplo:

```anim
circle repeat n 4:
start = n
origin = 0, -3 + n
radius = ln(n + 2)
```