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
```
<svg width="200" height="200">
</svg>
```
<svg width="200" height="200">
</svg>

### Line
```
<svg width="200" height="200">
</svg>
```
<svg width="200" height="200">
</svg>

### Polyline
```
<svg width="200" height="200">
</svg>
```
<svg width="200" height="200">
</svg>

### Polygon
```
<svg width="200" height="200">
</svg>
```
<svg width="200" height="200">
</svg>

### Path
```
<svg width="200" height="200">
</svg>
```
<svg width="200" height="200">
</svg>

## TODO
- Table of contents

[demo]: https://jcvar.github.io/svg-cheatsheet/
[tutorial]: https://developer.mozilla.org/en-US/docs/Web/SVG/Tutorial
