# Class `scene`
configures the scene

Example:
```
@scene:
width = 500
height = 500
fps = 30
```

## Programs
- [fps](#program-fps)
- [end](#program-end)
- [width](#program-width)
- [height](#program-height)
- [origin](#program-origin)
- [unit](#program-unit)
- [scale](#program-scale)
## Program `fps`
sets the frames per second

Example:
```
fps = 30
```

### Commands
`default {value}`
- `value` the value

sets the value

Example:
```
value = default 30
value = 30 // equivalent form
```


## Program `end`
sets the end time of the scene

Example:
```
end = 100 // the scene will end at 100 seconds
```

### Commands
`default {value}`
- `value` the value

sets the value

Example:
```
value = default 30
value = 30 // equivalent form
```


## Program `width`
sets the scene width, in pixels

Example:
```
width = 500
```

### Commands
`default {value}`
- `value` the value

sets the value

Example:
```
value = default 30
value = 30 // equivalent form
```


## Program `height`
sets the scene height, in pixels

Example:
```
height = 500
```

### Commands
`default {value}`
- `value` the value

sets the value

Example:
```
value = default 30
value = 30 // equivalent form
```


## Program `origin`
sets the scene origin in the coordinate system, where both coordinates in the origin are in the range [0,1], and the value (0,0) is the top left corner

Example:
```
origin = 0.5, 0.5 // the origin is the center of the scene
origin = 0, 0 // the origin is the top left corner of the scene
origin = 1, 1 // the origin is the bottom right corner of the scene
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


## Program `unit`
sets the size of an unit in the coordinate system, in pixels

Example:
```
unit = 32, 32 // the unit is 32x32 pixels
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


## Program `scale`
sets the scale of the coordinate system in x and y. For x, 1 means right, -1 means left. For y, 1 means bottom, -1 means top.

Example:
```
scale = 1, -1 // units are scaled to the right and up
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


