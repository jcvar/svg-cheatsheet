<!-- PREAMBLE -->
<style>
svg { background-color: rgb(200, 200, 200); }
</style>
<!-- PREAMBLE -->

# Basic Shapes

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
