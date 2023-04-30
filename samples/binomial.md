# Distribución binomial

La distribución binomial es una forma de describir el número de éxitos
en una secuencia de ensayos independientes, donde cada ensayo tiene solo 
dos posibles resultados: éxito o fracaso. Esta distribución se caracteriza
por dos parámetros: el número de ensayos "n" y la probabilidad de éxito 
"p" en cada ensayo.

La fórmula de la distribución es la siguiente:

$$
P(X = k) = \binom{n}{k} p^k (1-p)^{n-k}
$$

Que mide la probabilidad de que la variable aleatoria $X$ presente
$k$ éxitos en un total de $n$ ensayos, dada una probabilidad de éxito $p$
por cada ensayo.


En la siguiente animación, se puede visualizar la probabilidad de éxito
(eje vertical) en función del número de ensayos (eje horizontal).
La forma de esta gráfica se conoce como "campana de gauss":

```anim
// opciones de la escena
@scene:
width  = 480
height = 160
origin = 0.15, 0.8 // origen de los ejes relativo a la escena
unit   = 16, 16    // valor de una unidad, en pixeles
x_axis = positive  
y_axis = value binmax(20, 0.5)/6 positive 
axis_color = blue

// valores de la función de probabilidad
rectangle repeat n 20:
start  = 0.5 + n/10  // iniciar uno a uno
mode   = size        // definir rectángulo por su tamaño
origin = n, 0        // ubicar de izquierda a derecha
width  = 1           // todos los valores con el mismo ancho

// altura según su probabilidad
height = from 0 to 6*binnorm(20, n, 0.5) in 1 
// rellenar con un mapa de calor según la probabilidad
style = fill background = heat(red, green, 1, binnorm(20, n, 0.5))
```

Se puede también definir una función de probabilidad acumulada, la cual 
mide "la probabilidad de obtener $k$ **o menos** éxitos en un total 
de $n$ ensayos", cuya función se puede visualizar a continuación:

```anim
// opciones de la escena
@scene:
width  = 480
height = 160
origin = 0.15, 0.8 // origen de los ejes relativo a la escena
unit   = 16, 16    // valor de una unidad, en pixeles
x_axis = positive  
y_axis = value 1/6 positive 
axis_color = blue

// valores de la función de probabilidad
rectangle repeat n 20:
start  = 0.5 + n/10  // iniciar uno a uno
mode   = size        // definir rectángulo por su tamaño
origin = n, 0        // ubicar de izquierda a derecha
width  = 1           // todos los valores con el mismo ancho

// altura según su probabilidad acumulada
height = from 0 to 6*bincdf(20, n, 0.5) in 1 
// rellenar con un mapa de calor según la probabilidad
style = fill background = heat(red, green, 1, bincdf(20, n, 0.5))

// límite superior
segment:
border = red
origin = 0, 6 destination = 30, 6
```
