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

## Basic Shapes

### Rectangle
Start off simple: x, y, width and height. rx and ry set round corners.
```
<svg width="200" height="200">
    <rect x="10" y="10" width="30" height="30"/>
    <rect x="60" y="10" width="30" height="30" rx="10" ry="10"/>
</svg>
```
<svg width="200" height="200">
    <rect x="10" y="10" width="30" height="30"/>
    <rect x="60" y="10" width="30" height="30" rx="10" ry="10"/>
</svg>

### Circle
Coordinates of center and radius.
```
<svg width="200" height="200">
    <circle cx="25" cy="75" r="20"/>
</svg>
```
<svg width="200" height="200">
    <circle cx="25" cy="75" r="20"/>
</svg>

### Ellipse
Coordinates of center and radius on both axes.
```
<svg width="200" height="200">
    <ellipse cx="75" cy="75" rx="20" ry="5"/>
</svg>
```
<svg width="200" height="200">
    <ellipse cx="75" cy="75" rx="20" ry="5"/>
</svg>

### Line
Two points.
```
<svg width="200" height="200">
    <line x1="10" x2="50" y1="110" y2="150"/>
</svg>
```
<svg width="200" height="200">
    <line x1="10" x2="50" y1="110" y2="150"/>
</svg>

### Polyline
Many points, with coordinates separated by spaces or commas.
```
<svg width="200" height="200">
    <polyline points="60, 110 65, 120 70, 115 75, 130 80, 125 85, 140 90, 135 95, 150 100, 145"/>
</svg>
```
<svg width="200" height="200">
    <polyline points="60, 110 65, 120 70, 115 75, 130 80, 125 85, 140 90, 135 95, 150 100, 145"/>
</svg>

### Polygon
Like a polyline, but closes the first and last points.
```
<svg width="200" height="200">
    <polygon points="50, 160 55, 180 70, 180 60, 190 65, 205 50, 195 35, 205 40, 190 30, 180 45, 180"/>
</svg>
```
<svg width="200" height="200">
    <polygon points="50, 160 55, 180 70, 180 60, 190 65, 205 50, 195 35, 205 40, 190 30, 180 45, 180"/>
</svg>

### Path
Paths offer the most flexibility and are defined by a single attribute.
```
<svg width="200" height="200">
    <path d="M20,230 Q40,205 50,230 T90,230" fill="none" stroke="blue" stroke-width="5"/>
</svg>
```
<svg width="200" height="200">
    <path d="M20,230 Q40,205 50,230 T90,230" fill="none" stroke="blue" stroke-width="5"/>
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

There are two B??zier Curves and an Arc.

#### Cubic B??zier
Two control points, for the start and end slopes, and the end coordinate.
```
C x1 y1, x2 y2, x y
```

When chaining B??zier curves, and the next control point is a reflection of the
last, the cubic B??zier shortcut may be used. If it doesn't follows a `C` or `S`,
it's equivalent to a `Q`
```
S x2 y2, x y
```

#### Quadratic B??zier
One control point and end coordinate.
Relative (`q`) end point coordinates are relative to the start.
```
Q x1 y1, x y
```

As with the cubic B??zier, the control point can be the reflection of the last.
If it doesn't follow a `Q` or `T`, it's equivalent to a line.
```
T x y
```

## TODO
- Table of contents (GitHub now offers them anyway)

[demo]: https://jcvar.github.io/svg-cheatsheet/
[tutorial]: https://developer.mozilla.org/en-US/docs/Web/SVG/Tutorial
