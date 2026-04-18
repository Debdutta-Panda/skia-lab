# Canvas Apis
We will discuss about canvas apis

## Clear
Fills clip with color, means the whole canvas(clipped zone, if applied) with the given color.

`void clear(SkColor color)`
`void clear(const SkColor4f& color)`

Use `SkColorSetRGB(r,g,b)` to create your color and use to clear the canvas.

Example: `canvas->clear(SkColorSetRGB(244, 241, 234));`