# Fill and Stroke Attributes

### Painting
"Using `fill` sets the color inside the object and
`stroke` sets the color of the line drawn around the object."

Canvas like.

```
<svg>
    <rect x="10" y="10" width="100" height="100" stroke="blue" fill="purple"
        fill-opacity="0.5" stroke-opacity="0.8"/>
</svg>
```
<svg>
    <rect x="10" y="10" width="100" height="100" stroke="blue" fill="purple"
        fill-opacity="0.5" stroke-opacity="0.8"/>
</svg>

**Note:** `fill` and `stroke` opacity can be set independently. Or `rbga` in Firefox.

### Stroke
- `stroke-width`: width extends on both sides of the path

```
<svg width="160" height="140" xmlns="http://www.w3.org/2000/svg" version="1.1">
  <line x1="40" x2="120" y1="20" y2="20" stroke="black" stroke-width="20" stroke-linecap="butt"/>
  <line x1="40" x2="120" y1="60" y2="60" stroke="black" stroke-width="20" stroke-linecap="square"/>
  <line x1="40" x2="120" y1="100" y2="100" stroke="black" stroke-width="20" stroke-linecap="round"/>
</svg>
```
<svg width="160" height="140" xmlns="http://www.w3.org/2000/svg" version="1.1">
  <line x1="40" x2="120" y1="20" y2="20" stroke="black" stroke-width="20" stroke-linecap="butt"/>
  <line x1="40" x2="120" y1="60" y2="60" stroke="black" stroke-width="20" stroke-linecap="square"/>
  <line x1="40" x2="120" y1="100" y2="100" stroke="black" stroke-width="20" stroke-linecap="round"/>
</svg>
- `stroke-linecap`:
  - `butt` limits line end at path end
  - `square` projects half `stroke-width`
  - `round` round end with half `stroke-width` radius

```
<?xml version="1.0" standalone="no"?>
<svg width="160" height="280" xmlns="http://www.w3.org/2000/svg" version="1.1">
  <polyline points="40 60 80 20 120 60" stroke="black" stroke-width="20"
      stroke-linecap="butt" fill="none" stroke-linejoin="miter"/>

  <polyline points="40 140 80 100 120 140" stroke="black" stroke-width="20"
      stroke-linecap="round" fill="none" stroke-linejoin="round"/>

  <polyline points="40 220 80 180 120 220" stroke="black" stroke-width="20"
      stroke-linecap="square" fill="none" stroke-linejoin="bevel"/>
</svg>
```
<svg width="160" height="280" xmlns="http://www.w3.org/2000/svg" version="1.1">
  <polyline points="40 60 80 20 120 60" stroke="black" stroke-width="20"
      stroke-linecap="butt" fill="none" stroke-linejoin="miter"/>

  <polyline points="40 140 80 100 120 140" stroke="black" stroke-width="20"
      stroke-linecap="round" fill="none" stroke-linejoin="round"/>

  <polyline points="40 220 80 180 120 220" stroke="black" stroke-width="20"
      stroke-linecap="square" fill="none" stroke-linejoin="bevel"/>
</svg>
- `stroke-linejoin`:
  - `miter` extends line ends to form a single angle
  - `round` round end (with half `stroke-width` radius too)
  - `bevel` joins projects half `stroke-width`

