# Segmento

## 1.1. Extremos del segmento

Los puntos extremos de un segmento pueden ser decorados con diferentes figuras. A continuación se describe el procedimiento para generar dichas decoraciones.


### 1.1.1. Flechas
La decoración de flechas requiere los siguientes parámetros:

- Longitud de las diagonales de la flecha ($d$).
- Ángulo entre cada diagonal y el segmento ($\beta$).

El primer paso consiste en obtener el ángulo $\alpha$ formado entre el punto de origen $(x_1, y_1)$ y de destino $(x_2, y_2)$ del segmento. Un vez obtenido, se calcula el ángulo del punto extremo a cada diagonal de la flecha, de la siguiente forma:

$$
\alpha_1 = \alpha + \beta \\
\alpha_2 = \alpha - \beta
$$

Lo siguiente es obtener las coordenadas de los puntos extremos de las diagonales de la flecha, de la siguiente forma:

$$
E_1 = \begin{pmatrix}
    x_1 + d \cdot \cos(\alpha_1) \\
    y_1 + d \cdot \sin(\alpha_1) 
\end{pmatrix}
$$

$$
E_2 = \begin{pmatrix}
    x_1 + d \cdot \cos(\alpha_2) \\
    y_1 + d \cdot \sin(\alpha_2)
\end{pmatrix}
$$

Y finalmente, el dibujo de la flecha se realiza como un polígono entre el origen $(x_1, y_1)$ y los dos extremos calculados $E_1$ y $E_2$.

Si la flecha debe dibujarse en el destino en lugar del origen, basta con rotar media circunferencia ($180°$) los ángulos $\alpha_1$ y $\alpha_2$.

### 1.1.2. Círculos
Esta es la más simple de las decoraciones, el único parámetro que requiere es el radio del círculo ($r$). Se debe dibujar un arco de circunferencia centrado en cualquiera de los puntos extremos del segmento con el radio indicado.

### 1.1.3. Rectas
Esta decoración consiste en dibujar una línea perpendicular al segmento en sus dos puntos extremos. Para ello, se debe calcular el ángulo de cada uno de los extremos de la línea perpendicular con respecto al segmento, de la siguiente forma:

$$
\alpha_1 = \alpha + \frac{\pi}{2} \\
\alpha_2 = \alpha - \frac{\pi}{2}
$$

Luego, se calculan las coordenadas de los puntos extremos de la línea perpendicular, de la siguiente forma:

$$
E_1 = \begin{pmatrix}
    x_1 + r \cdot \cos(\alpha_1) \\
    y_1 + r \cdot \sin(\alpha_1)
\end{pmatrix}
$$

$$
E_2 = \begin{pmatrix}
    x_1 + r \cdot \cos(\alpha_2) \\
    y_1 + r \cdot \sin(\alpha_2)
\end{pmatrix}
$$

Finalmente, el dibujo consiste en trazar una línea entre los dos puntos extremos calculados $E_1$ y $E_2$.

Es importante aclarar que estas operaciones deberían realizarse **después** de realizar las transformaciones de sistema de coordenadas correspondientes.