# svg-cheatsheet

Learning SVG with the [MDN Tutorial][tutorial].

GitHub doesn't render SVGs in `.md` files. See them on GitHub Pages [here][demo].


<style>
svg { background-color: rgb(200, 200, 200); }
</style>
Example template:
```
<svg width="200" height="200">
</svg>
```
<svg width="200" height="200">
</svg>

## Paths
Paths are composed of multiple commands inside the `d` attribute.
Each command is represented by a letter and followed by some parameters.

- Uppercase letters specify absolute coordinates.
- Lowercase letters specify coordinates relative to the last point.

### Line commands

#### M - Move to
Moves the cursor to a specific coordinate, with no trace.
```
M x y
```

#### L - Line to
Draws a line to the specified coordinate, from the current position.
```
L x y
```

#### H - Horizontal line
Draw a horizontal line to an x coordinate. (h: of x length)
```
H x
```

#### V - Vertical line
Draw a vertical line to a y coordinate. (v: of y length)
```
V y
```

#### Z - Close path
Draws a straight line from the cursor to the first point of the path.
Has no parameters or difference in behavior when lowercase.
```
Z
```

##### Examples
Absolute coordinates:
```
<svg width="100" height="100">
     <path d="M 10 10 H 90 V 90 H 10 Z" fill="transparent" stroke="black"/>
</svg>
```
<svg width="100" height="100">
     <path d="M 10 10 H 90 V 90 H 10 Z" fill="transparent" stroke="black"/>
</svg>

Relative coordinates:
```
<svg width="100" height="100">
     <path d="M 10 10 h 80 v 80 h -80 z" fill="transparent" stroke="black"/>
</svg>
```
<svg width="100" height="100">
     <path d="M 10 10 h 80 v 80 h -80 z" fill="transparent" stroke="black"/>
</svg>

### Curve commands

There are two Bézier Curves and an Arc.

#### Cubic Bézier
Two control points, for the start and end slopes, and the end coordinate.
```
C x1 y1, x2 y2, x y
```

When chaining Bézier curves, and the next control point is a reflection of the
last, the cubic Bézier shortcut may be used. If it doesn't follows a `C` or `S`,
it's equivalent to a `Q`
```
S x2 y2, x y
```

#### Quadratic Bézier
One control point and end coordinate.
Relative (`q`) end point coordinates are relative to the start.
```
Q x1 y1, x y
```

As with the cubic Bézier, the control point can be the reflection of the last.
If it doesn't follow a `Q` or `T`, it's equivalent to a line.
```
T x y
```

## TODO
- Table of contents (GitHub now offers them anyway)

[demo]: https://jcvar.github.io/svg-cheatsheet/
[tutorial]: https://developer.mozilla.org/en-US/docs/Web/SVG/Tutorial
