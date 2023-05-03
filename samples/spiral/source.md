# Espiral logarítmica

```anim
@scene:
height=320
fps=60

// Círculo en cada ubicación de la espiral
circle repeat i 36*3:
start = i/8                            // Cada círculo aparece cada 1/8 de segundo
radius = from 0 to (i+1)/(36*2) in 1/8 // Cada círculo crece gradualmente
origin = 
  from 0, 0 to                    // Comenzar en el origen
  1.1^(2*pi/36*i)*cos(2*pi/36*i), // Y moverse hacia la posición correspondiente
  1.1^(2*pi/36*i)*sin(2*pi/36*i)
  in 1/4

style = fill
background = heat(blue, red, 36*3, i) // Mapa de calor según la posición en la espiral
background_opacity = 0.5

// Flecha que va marcando el último círculo
segment repeat i 36*3:
start = i/8
end = (i + 1)/8
origin = 0, 0
destination = 
  1.1^(2*pi/36*i)*cos(2*pi/36*i), // apuntar hacia la posición correspondiente
  1.1^(2*pi/36*i)*sin(2*pi/36*i)

trail = arrow size 8
```

En coordenadas cartesianas, la curva de una espiral logarítmica se puede
representar con las siguientes ecuaciones:

$$
\begin{split}
x & = ab^\theta \cos{\theta} \\
y & = ab^\theta \sin{\theta} \\
\end{split}
$$

En donde $a$ y $b$ son factores que controlan el tamaño y crecimiento de 
la espiral, y $\theta$ es el ángulo sobre el cual se deseen calcular las
coordenadas.