# Construcción geométrica
## Estrella de curvas parabólicas

Se puede construir una estrella cuyos lados sean curvas similares 
a parábolas usando únicamente líneas rectas, como se muestra en
la siguiente ilustración:

```anim
@scene:
width = 800
height = 600
axis_color = black

segment repeat n 11: // Cuadrante superior derecho
start = n/2
origin = n, 0
destination = 
  from n, 0
    to 0, 10 - n
    in 0.5
border = heat(green, red, 10, n)

segment repeat n 11: // Cuadrante inferior derecho
start = n/2
origin = n, 0
destination = 
  from n, 0
    to 0, -(10 - n)
    in 0.5
border = heat(green, red, 10, n)

segment repeat n 11: // Cuadrante superior izquierdo
start = n/2
origin = -n, 0
destination = 
  from -n, 0
    to 0, 10 - n
    in 0.5
border = heat(green, red, 10, n)

segment repeat n 11: // Cuadrante inferior izquierdo
start = n/2
origin = -n, 0
destination = 
  from -n, 0
    to 0, -(10 - n)
    in 0.5
border = heat(green, red, 10, n)
```

La estrategia consiste en decidir una cantidad fija de segmentos a 
dibujar, véase $n$. Luego, para cada cuadrante se construyen los
siguientes segmentos $i$, tal que $0 \leq i \leq n$:

$$
\begin{split}
S_1(i) & = \left\{(0, i), (n - i, 0)\right\} \\
S_2(i) & = \left\{(0, -i), (n - i, 0)\right\} \\
S_3(i) & = \left\{(i, 0), (0, n - i)\right\} \\
S_3(i) & = \left\{(-i, 0), (0, n - i)\right\} \\
\end{split}
$$

Es decir, se debe conectar el primer punto en el eje horizontal con
el último en el vertical, el segundo con el penúltimo y así 
sucesivamente.

Fíjese con más detalle en el proceso, enfocado en solo uno de 
los cuadrantes:

```anim
@scene:
width = 640
height = 480
origin = 0.2, 0.8
axis_color = black
x_axis = positive
y_axis = positive

segment repeat n 11: 
start = 2*n
origin = n, 0
destination = 
  from n, 0
    to 0, 10 - n
    in 2
border = heat(green, red, 10, n)
```