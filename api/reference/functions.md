# Functions

## ln

```
ln(x)
```
Returns the natural logarithm of x.

## log2

```
log2(x)
```
Returns the base 2 logarithm of x.

## log10

```
log10(x)
```
Returns the base 10 logarithm of x.

## log

```
log(n, x)
```
Returns the base n logarithm of x.

## abs

```
abs(x)
```
Returns the absolute value of x.

## sign

```
sign(x)
```
Returns the sign of x. This is:
- 1 if x is positive
- 0 if x is zero
- -1 if x is negative

## floor

```
floor(x)
```
Returns the largest integer value less than or equal to x.

## ceil

```
ceil(x)
```
Returns the smallest integer value greater than or equal to x.

## round

```
round(x)
```
Returns the nearest integer value to x.

## min

```
min(x, y)
```
Returns the smaller of x and y.

## max

```
max(x, y)
```
Returns the larger of x and y.

## clamp

```
clamp(x, min, max)
```
Clamps x between min and max.

## lerp

```
lerp(x, y, t)
```
Linearly interpolates between x and y by t.

## pow

```
pow(x, y)
```
Returns x to the power of y (x^y).

## sqrt

```
sqrt(x)
```
Returns the square root of x.

## cbrt

```
cbrt(x)
```
Returns the cube root of x.

## sin

```
sin(x)
```
Returns the sine of x.

## cos

```
cos(x)
```
Returns the cosine of x.

## tan

```
tan(x)
```
Returns the tangent of x.

## asin

```
asin(x)
```
Returns the arcsine of x.

## acos

```
acos(x)
```
Returns the arccosine of x.

## atan

```
atan(x)
```
Returns the arctangent of x.

## atan2

```
atan2(y, x)
```
Returns the arctangent of y/x.

## rgb

```
rgb(r, g, b)
```
Returns a color with the given red, green, and blue components. Each component should be between 0 and 255.

## hsv

```
hsv(h, s, v)
```
Returns a color with the given hue, saturation, and value. Each component should be between 0 and 255.

## heat

```
heat(color_min, color_max, value_max, value)
```
Returns a color between color_min and color_max, based on the given value and the maximum values. 

## bin

```
bin(n, x, p)
```
Returns the binomial probability of exactly x successesin n trials, each with a probability p of success.

## bincdf

```
bincdf(n, x, p)
```
returns the binomial cumulative distribution function of x successes in n trials, each trial with probability p. This is the probability of getting x or fewer successes.

## bincdfc

```
bincdfc(n, x, p)
```
returns the binomial cumulative distribution function of x successes in n trials, each trial with probability p. This is the probability of getting x or more successes.

## binmax

```
binmax(n, p)
```
Returns the probability of the mean number of successes in n trials, each trial with probability p.

## binnorm

```
binnorm(n, x, p)
```
Returns a normalized value between 0 and 1 that represents the probability of x successes in n trials, each trial with probability p. Where 1 is the maximum probability, at the mean number of successes.

