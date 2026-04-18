# Canvas Apis
We will discuss about canvas apis

## Clear
Fills clip with color, means the whole canvas(clipped zone, if applied) with the given color.

`void clear(SkColor color)`
`void clear(const SkColor4f& color)`

Use `SkColorSetRGB(r,g,b)` to create your color and use to clear the canvas.

Example:
```cpp
canvas->clear(SkColorSetRGB(244, 120, 0));
```
<img width="946" height="633" alt="image" src="https://github.com/user-attachments/assets/6f9bd25d-195d-4efc-babc-285e8c008b4e" />

## DrawColor
If you want control on blend mode to clear the whole clipped area then you should use `drawColor`.

`void drawColor(SkColor color, SkBlendMode mode = SkBlendMode::kSrcOver)`

`void drawColor(const SkColor4f& color, SkBlendMode mode = SkBlendMode::kSrcOver)`

Example:
```cpp
canvas->drawColor(SkColorSetARGB(255, 244, 120, 0), SkBlendMode::kSrc);
canvas->drawColor(SkColorSetARGB(255, 0, 120, 0), SkBlendMode::kColorDodge);
```