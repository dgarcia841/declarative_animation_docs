# Class `polygon`
Configures a polygon object

Example:
```
polygon:
origin = from 0, 0 to 100, 0 in 1.5 // animate the origin point
radius = from 0 to 100 in 1.5 // animate the radius
sides = from 3 to 5 in 1.5 // animate the number of sides
```

## Programs
- [start](#program-start)
- [end](#program-end)
- [fig_origin](#program-fig_origin)
- [fig_rotation](#program-fig_rotation)
- [fig_scale](#program-fig_scale)
- [background](#program-background)
- [background_opacity](#program-background_opacity)
- [border](#program-border)
- [border_opacity](#program-border_opacity)
- [origin](#program-origin)
- [radius](#program-radius)
- [sides](#program-sides)
- [style](#program-style)
## Program `start`
Sets the time before the animation starts, in seconds

### Commands
`default {time}`
- `time` time before the animation starts, in seconds

Sets the time before the animation starts, in seconds

Example:
```
start = 1.5 // starts after 1.5 seconds
```


## Program `end`
Sets the time after the animation ends, in seconds

### Commands
`default {time}`
- `time` time after the animation ends, in seconds

Sets the time after the animation ends, in seconds

Example:
```
end = 1.5 // ends after 1.5 seconds
```


## Program `fig_origin`
Sets the origin of the figure for transformations

Example:
```
fig_origin = 0.5, 0.5 // sets the origin to the center of the figure
```

### Commands
`from {x} {y}`
- `x` Horizontal position

- `y` Vertical position

Sets the starting position (x, y) of the vector

Example:
```
from 0, 0
```

`to {x} {y}`
- `x` Horizontal position

- `y` Vertical position

Sets the ending position (x, y) of the vector

Example:
```
to 100, 100
```

`in {duration}`
- `duration` time between positions change

Sets the duration (time) of the animation from the starting position to the ending position

Example:
```
in 1.5
```

`pivot {x} {y}`
- `x` Horizontal position

- `y` Vertical position

Sets the rotation center of the animation. If defined, the vector will rotate around this point to move from the starting position to the ending position, instead of moving in a straight line.

Example:
```
pivot 50, 50
```

`shortspin`
Sets the animation to rotate around the pivot point using the shortest path.

Example:
```
shortspin
```

`longspin`
Sets the animation to rotate around the pivot point using the longest path.

Example:
```
longspin
```

`default {x} {y}`
- `x` Horizontal position

- `y` Vertical position

Sets the default position (x, y) of the vector

Example:
```
default 0, 0
```

`stop`
On end, the animation will stop

`restart`
On end, the animation will restart

`reverse`
On end, the animation will reverse

`linear`
Uses a linear function for this transition

Example:
```
radius = from 1 to 10 linear // linear transition
```

`accel1 {initial_speed}`
- `initial_speed` the initial speed of the transition

Uses an acceleration function for this transition. The animation will start at a given speed, and will accelerate at constant rate until it reaches the final value.

Example:
```
radius = from 1 to 10 accel1 0.1 // acceleration transition
```

`accel2 {initial_speed}`
- `initial_speed` the initial speed of the transition

Uses an acceleration function for this transition. The animation will start at a given speed, accelerate at constant rate until it reaches max speed at the middle of the transition, and then decelerate at constant rate until it reaches the final value.

Example:
```
radius = from 1 to 10 accel2 0.1 // acceleration transition
```


## Program `fig_rotation`
Sets the rotation of the figure, in radians

Example:
```
fig_rotation = 0.5 // rotates the figure by 0.5 radians
```

### Commands
`from {x}`
- `x` Starting value

Sets the starting value of the value

Example:
```
from 0
```

`to {x}`
- `x` Ending value

Sets the ending value of the value

Example:
```
to 100
```

`in {duration}`
- `duration` time between values change

Sets the duration (time) of the animation from the starting value to the ending value

Example:
```
in 1.5
```

`default {x}`
- `x` Default value

Sets the default value of the value

Example:
```
default 0
```

`stop`
On end, the animation will stop

`restart`
On end, the animation will restart

`reverse`
On end, the animation will reverse

`linear`
Uses a linear function for this transition

Example:
```
radius = from 1 to 10 linear // linear transition
```

`accel1 {initial_speed}`
- `initial_speed` the initial speed of the transition

Uses an acceleration function for this transition. The animation will start at a given speed, and will accelerate at constant rate until it reaches the final value.

Example:
```
radius = from 1 to 10 accel1 0.1 // acceleration transition
```

`accel2 {initial_speed}`
- `initial_speed` the initial speed of the transition

Uses an acceleration function for this transition. The animation will start at a given speed, accelerate at constant rate until it reaches max speed at the middle of the transition, and then decelerate at constant rate until it reaches the final value.

Example:
```
radius = from 1 to 10 accel2 0.1 // acceleration transition
```


## Program `fig_scale`
Sets the scale of the figure

Example:
```
fig_scale = 0.5, 0.5 // scales the figure by 0.5 in both directions
```

### Commands
`from {x} {y}`
- `x` Horizontal position

- `y` Vertical position

Sets the starting position (x, y) of the vector

Example:
```
from 0, 0
```

`to {x} {y}`
- `x` Horizontal position

- `y` Vertical position

Sets the ending position (x, y) of the vector

Example:
```
to 100, 100
```

`in {duration}`
- `duration` time between positions change

Sets the duration (time) of the animation from the starting position to the ending position

Example:
```
in 1.5
```

`pivot {x} {y}`
- `x` Horizontal position

- `y` Vertical position

Sets the rotation center of the animation. If defined, the vector will rotate around this point to move from the starting position to the ending position, instead of moving in a straight line.

Example:
```
pivot 50, 50
```

`shortspin`
Sets the animation to rotate around the pivot point using the shortest path.

Example:
```
shortspin
```

`longspin`
Sets the animation to rotate around the pivot point using the longest path.

Example:
```
longspin
```

`default {x} {y}`
- `x` Horizontal position

- `y` Vertical position

Sets the default position (x, y) of the vector

Example:
```
default 0, 0
```

`stop`
On end, the animation will stop

`restart`
On end, the animation will restart

`reverse`
On end, the animation will reverse

`linear`
Uses a linear function for this transition

Example:
```
radius = from 1 to 10 linear // linear transition
```

`accel1 {initial_speed}`
- `initial_speed` the initial speed of the transition

Uses an acceleration function for this transition. The animation will start at a given speed, and will accelerate at constant rate until it reaches the final value.

Example:
```
radius = from 1 to 10 accel1 0.1 // acceleration transition
```

`accel2 {initial_speed}`
- `initial_speed` the initial speed of the transition

Uses an acceleration function for this transition. The animation will start at a given speed, accelerate at constant rate until it reaches max speed at the middle of the transition, and then decelerate at constant rate until it reaches the final value.

Example:
```
radius = from 1 to 10 accel2 0.1 // acceleration transition
```


## Program `background`
Sets the background color of the figure. The colors are expressed in format of 24 bits numbers, where the first 8 bits are for the red channel, the next 8 bits are for the green channel and the last 8 bits are for the blue channel. You can also use the hexadecimal format, where the first 2 digits are for the red channel, the next 2 digits are for the green channel and the last 2 digits are for the blue channel. Functions `rgb(r, g, b)` and `hsv(h, s, v)` can also be used.

Example:
```
background = #ff0000 // red
background = from #ff0000 to #00ff00 in 1 // from red to green in 1 second
background = rgb(255, 0, 0) // red
background = from rgb(255, 0, 0) to rgb(0, 255, 0) in 1 // from red to green in 1 second
```

### Commands
`from {xyz}`
- `xyz` 24-bit integer representing x, y, z values

Sets the starting point (x, y, z) of the vector 3D using a single number, where the first 8 bits are the value of x, the second 8 bits are the value of y, and the last 8 bits are the value of z.

Example:
```
from #ff0000
from 16711680
```

`to {xyz}`
- `xyz` 24-bit integer representing x, y, z values

Sets the ending point (x, y, z) of the vector 3D using a single number, where the first 8 bits are the value of x, the second 8 bits are the value of y, and the last 8 bits are the value of z.

Example:
```
to #ff0000
to 16711680
```

`in {duration}`
- `duration` _no description_

Sets the duration (time) of the animation from the starting point to the ending point

Example:
```
in 1.5
```

`default {xyz}`
- `xyz` 24-bit integer representing x, y, z values

Sets the default value of the vector 3D using a single number, where the first 8 bits are the value of x, the second 8 bits are the value of y, and the last 8 bits are the value of z.

Example:
```
default #ff0000
default 16711680
```

`stop`
On end, the animation will stop

`restart`
On end, the animation will restart

`reverse`
On end, the animation will reverse

`linear`
Uses a linear function for this transition

Example:
```
radius = from 1 to 10 linear // linear transition
```

`accel1 {initial_speed}`
- `initial_speed` the initial speed of the transition

Uses an acceleration function for this transition. The animation will start at a given speed, and will accelerate at constant rate until it reaches the final value.

Example:
```
radius = from 1 to 10 accel1 0.1 // acceleration transition
```

`accel2 {initial_speed}`
- `initial_speed` the initial speed of the transition

Uses an acceleration function for this transition. The animation will start at a given speed, accelerate at constant rate until it reaches max speed at the middle of the transition, and then decelerate at constant rate until it reaches the final value.

Example:
```
radius = from 1 to 10 accel2 0.1 // acceleration transition
```


## Program `background_opacity`
Sets the background opacity of the figure

Example:
```
background_opacity = 0.5 // half transparent
background_opacity = from 0.5 to 1 in 1 // from half transparent to fully transparent in 1 second
```

### Commands
`from {x}`
- `x` Starting value

Sets the starting value of the value

Example:
```
from 0
```

`to {x}`
- `x` Ending value

Sets the ending value of the value

Example:
```
to 100
```

`in {duration}`
- `duration` time between values change

Sets the duration (time) of the animation from the starting value to the ending value

Example:
```
in 1.5
```

`default {x}`
- `x` Default value

Sets the default value of the value

Example:
```
default 0
```

`stop`
On end, the animation will stop

`restart`
On end, the animation will restart

`reverse`
On end, the animation will reverse

`linear`
Uses a linear function for this transition

Example:
```
radius = from 1 to 10 linear // linear transition
```

`accel1 {initial_speed}`
- `initial_speed` the initial speed of the transition

Uses an acceleration function for this transition. The animation will start at a given speed, and will accelerate at constant rate until it reaches the final value.

Example:
```
radius = from 1 to 10 accel1 0.1 // acceleration transition
```

`accel2 {initial_speed}`
- `initial_speed` the initial speed of the transition

Uses an acceleration function for this transition. The animation will start at a given speed, accelerate at constant rate until it reaches max speed at the middle of the transition, and then decelerate at constant rate until it reaches the final value.

Example:
```
radius = from 1 to 10 accel2 0.1 // acceleration transition
```


## Program `border`
Sets the border color of the figure The colors are expressed in format of 24 bits numbers, where the first 8 bits are for the red channel, the next 8 bits are for the green channel and the last 8 bits are for the blue channel. You can also use the hexadecimal format, where the first 2 digits are for the red channel, the next 2 digits are for the green channel and the last 2 digits are for the blue channel. Functions `rgb(r, g, b)` and `hsv(h, s, v)` can also be used.

Example:
```
border = #ff0000 // red
border = from #ff0000 to #00ff00 in 1 // from red to green in 1 second
border = rgb(255, 0, 0) // red
border = from rgb(255, 0, 0) to rgb(0, 255, 0) in 1 // from red to green in 1 second
```

### Commands
`from {xyz}`
- `xyz` 24-bit integer representing x, y, z values

Sets the starting point (x, y, z) of the vector 3D using a single number, where the first 8 bits are the value of x, the second 8 bits are the value of y, and the last 8 bits are the value of z.

Example:
```
from #ff0000
from 16711680
```

`to {xyz}`
- `xyz` 24-bit integer representing x, y, z values

Sets the ending point (x, y, z) of the vector 3D using a single number, where the first 8 bits are the value of x, the second 8 bits are the value of y, and the last 8 bits are the value of z.

Example:
```
to #ff0000
to 16711680
```

`in {duration}`
- `duration` _no description_

Sets the duration (time) of the animation from the starting point to the ending point

Example:
```
in 1.5
```

`default {xyz}`
- `xyz` 24-bit integer representing x, y, z values

Sets the default value of the vector 3D using a single number, where the first 8 bits are the value of x, the second 8 bits are the value of y, and the last 8 bits are the value of z.

Example:
```
default #ff0000
default 16711680
```

`stop`
On end, the animation will stop

`restart`
On end, the animation will restart

`reverse`
On end, the animation will reverse

`linear`
Uses a linear function for this transition

Example:
```
radius = from 1 to 10 linear // linear transition
```

`accel1 {initial_speed}`
- `initial_speed` the initial speed of the transition

Uses an acceleration function for this transition. The animation will start at a given speed, and will accelerate at constant rate until it reaches the final value.

Example:
```
radius = from 1 to 10 accel1 0.1 // acceleration transition
```

`accel2 {initial_speed}`
- `initial_speed` the initial speed of the transition

Uses an acceleration function for this transition. The animation will start at a given speed, accelerate at constant rate until it reaches max speed at the middle of the transition, and then decelerate at constant rate until it reaches the final value.

Example:
```
radius = from 1 to 10 accel2 0.1 // acceleration transition
```


## Program `border_opacity`
Sets the border opacity of the figure

Example:
```
border_opacity = 0.5 // half transparent
border_opacity = from 0.5 to 1 in 1 // from half transparent to fully transparent in 1 second
```

### Commands
`from {x}`
- `x` Starting value

Sets the starting value of the value

Example:
```
from 0
```

`to {x}`
- `x` Ending value

Sets the ending value of the value

Example:
```
to 100
```

`in {duration}`
- `duration` time between values change

Sets the duration (time) of the animation from the starting value to the ending value

Example:
```
in 1.5
```

`default {x}`
- `x` Default value

Sets the default value of the value

Example:
```
default 0
```

`stop`
On end, the animation will stop

`restart`
On end, the animation will restart

`reverse`
On end, the animation will reverse

`linear`
Uses a linear function for this transition

Example:
```
radius = from 1 to 10 linear // linear transition
```

`accel1 {initial_speed}`
- `initial_speed` the initial speed of the transition

Uses an acceleration function for this transition. The animation will start at a given speed, and will accelerate at constant rate until it reaches the final value.

Example:
```
radius = from 1 to 10 accel1 0.1 // acceleration transition
```

`accel2 {initial_speed}`
- `initial_speed` the initial speed of the transition

Uses an acceleration function for this transition. The animation will start at a given speed, accelerate at constant rate until it reaches max speed at the middle of the transition, and then decelerate at constant rate until it reaches the final value.

Example:
```
radius = from 1 to 10 accel2 0.1 // acceleration transition
```


## Program `origin`
Configures the origin point of the polygon

Example:
```
origin = from 0, 0 to 100, 0 in 1.5 // animate the origin point
```

### Commands
`from {x} {y}`
- `x` Horizontal position

- `y` Vertical position

Sets the starting position (x, y) of the vector

Example:
```
from 0, 0
```

`to {x} {y}`
- `x` Horizontal position

- `y` Vertical position

Sets the ending position (x, y) of the vector

Example:
```
to 100, 100
```

`in {duration}`
- `duration` time between positions change

Sets the duration (time) of the animation from the starting position to the ending position

Example:
```
in 1.5
```

`pivot {x} {y}`
- `x` Horizontal position

- `y` Vertical position

Sets the rotation center of the animation. If defined, the vector will rotate around this point to move from the starting position to the ending position, instead of moving in a straight line.

Example:
```
pivot 50, 50
```

`shortspin`
Sets the animation to rotate around the pivot point using the shortest path.

Example:
```
shortspin
```

`longspin`
Sets the animation to rotate around the pivot point using the longest path.

Example:
```
longspin
```

`default {x} {y}`
- `x` Horizontal position

- `y` Vertical position

Sets the default position (x, y) of the vector

Example:
```
default 0, 0
```

`stop`
On end, the animation will stop

`restart`
On end, the animation will restart

`reverse`
On end, the animation will reverse

`linear`
Uses a linear function for this transition

Example:
```
radius = from 1 to 10 linear // linear transition
```

`accel1 {initial_speed}`
- `initial_speed` the initial speed of the transition

Uses an acceleration function for this transition. The animation will start at a given speed, and will accelerate at constant rate until it reaches the final value.

Example:
```
radius = from 1 to 10 accel1 0.1 // acceleration transition
```

`accel2 {initial_speed}`
- `initial_speed` the initial speed of the transition

Uses an acceleration function for this transition. The animation will start at a given speed, accelerate at constant rate until it reaches max speed at the middle of the transition, and then decelerate at constant rate until it reaches the final value.

Example:
```
radius = from 1 to 10 accel2 0.1 // acceleration transition
```


## Program `radius`
Configures the radius of the polygon

Example:
```
radius = from 0 to 100 in 1.5 // animate the radius
```

### Commands
`from {x}`
- `x` Starting value

Sets the starting value of the value

Example:
```
from 0
```

`to {x}`
- `x` Ending value

Sets the ending value of the value

Example:
```
to 100
```

`in {duration}`
- `duration` time between values change

Sets the duration (time) of the animation from the starting value to the ending value

Example:
```
in 1.5
```

`default {x}`
- `x` Default value

Sets the default value of the value

Example:
```
default 0
```

`stop`
On end, the animation will stop

`restart`
On end, the animation will restart

`reverse`
On end, the animation will reverse

`linear`
Uses a linear function for this transition

Example:
```
radius = from 1 to 10 linear // linear transition
```

`accel1 {initial_speed}`
- `initial_speed` the initial speed of the transition

Uses an acceleration function for this transition. The animation will start at a given speed, and will accelerate at constant rate until it reaches the final value.

Example:
```
radius = from 1 to 10 accel1 0.1 // acceleration transition
```

`accel2 {initial_speed}`
- `initial_speed` the initial speed of the transition

Uses an acceleration function for this transition. The animation will start at a given speed, accelerate at constant rate until it reaches max speed at the middle of the transition, and then decelerate at constant rate until it reaches the final value.

Example:
```
radius = from 1 to 10 accel2 0.1 // acceleration transition
```


## Program `sides`
Configures the number of sides of the polygon

Example:
```
sides = from 3 to 5 in 1.5 // animate the number of sides
```

### Commands
`from {x}`
- `x` Starting value

Sets the starting value of the value

Example:
```
from 0
```

`to {x}`
- `x` Ending value

Sets the ending value of the value

Example:
```
to 100
```

`in {duration}`
- `duration` time between values change

Sets the duration (time) of the animation from the starting value to the ending value

Example:
```
in 1.5
```

`default {x}`
- `x` Default value

Sets the default value of the value

Example:
```
default 0
```

`stop`
On end, the animation will stop

`restart`
On end, the animation will restart

`reverse`
On end, the animation will reverse

`linear`
Uses a linear function for this transition

Example:
```
radius = from 1 to 10 linear // linear transition
```

`accel1 {initial_speed}`
- `initial_speed` the initial speed of the transition

Uses an acceleration function for this transition. The animation will start at a given speed, and will accelerate at constant rate until it reaches the final value.

Example:
```
radius = from 1 to 10 accel1 0.1 // acceleration transition
```

`accel2 {initial_speed}`
- `initial_speed` the initial speed of the transition

Uses an acceleration function for this transition. The animation will start at a given speed, accelerate at constant rate until it reaches max speed at the middle of the transition, and then decelerate at constant rate until it reaches the final value.

Example:
```
radius = from 1 to 10 accel2 0.1 // acceleration transition
```


## Program `style`
Configures the style of the figure. The styles can be fill, stroke, or both. A filled figure is a figure with a color inside, and a stroked figure is a figure with a color outline. By default, the figures are stroked but not filled.

Example:
```
style = fill // fill the figure
style = stroke // stroke the figure
style = fill stroke // fill and stroke the figure
style = nofill nostroke // do not fill or stroke the figure
```

### Commands
`fill`
Enables the fill of the figure

Example:
```
style = fill
```

`nofill`
Disables the fill of the figure

Example:
```
style = nofill
```

`stroke`
Enables the stroke of the figure

Example:
```
style = stroke
```

`nostroke`
Disables the stroke of the figure

Example:
```
style = nostroke
```


