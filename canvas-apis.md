<link rel="stylesheet" href="/assets/css/style.css">

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
<img width="400" alt="image" src="https://github.com/user-attachments/assets/6f9bd25d-195d-4efc-babc-285e8c008b4e" />

## DrawColor
If you want control on blend mode to clear the whole clipped area then you should use `drawColor`.

`void drawColor(SkColor color, SkBlendMode mode = SkBlendMode::kSrcOver)`

`void drawColor(const SkColor4f& color, SkBlendMode mode = SkBlendMode::kSrcOver)`

Example:
```cpp
canvas->drawColor(SkColorSetARGB(255, 244, 120, 0), SkBlendMode::kSrc);
canvas->drawColor(SkColorSetARGB(255, 0, 120, 0), SkBlendMode::kColorDodge);
```
<img width="400" alt="image" src="https://github.com/user-attachments/assets/b0cd4120-05f5-49ca-affe-14f08b460838" />

# Paint
Paint is the container of many configurations for a painting like:
* color
* gradient
* stroke width
* stroke style, etc

Example:
```cpp
SkPaint paint;
paint.setColor(SK_ColorRED);
```
# DrawLine
`void drawLine(SkScalar x0, SkScalar y0, SkScalar x1, SkScalar y1, const SkPaint& paint)`

`void drawLine(SkPoint p0, SkPoint p1, const SkPaint& paint)`

Example:
```cpp
canvas->clear(SK_ColorWHITE);
SkPaint paint;
paint.setColor(SK_ColorRED);
canvas->drawLine(20, 20, 40, 40, paint);
```

<img width="400" alt="image" src="https://github.com/user-attachments/assets/df7c2578-08e6-4cca-8ef2-d90ce4dc6d71" />

# DrawRect

`void drawRect(const SkRect& rect, const SkPaint& paint)`

Example:
```cpp
canvas->clear(SK_ColorWHITE);
SkPaint paint;
paint.setColor(SK_ColorRED);
SkRect rect = {100,100,200,200};
canvas->drawRect(rect, paint);
```

<img width="400" alt="image" src="https://github.com/user-attachments/assets/a8749841-2680-4a3e-b1d1-140ef81c4a68" />

# DrawOval

`void drawOval(const SkRect& oval, const SkPaint& paint)`

Example:
```cpp
canvas->clear(SK_ColorWHITE);
SkPaint paint;
paint.setColor(SK_ColorRED);
SkRect rect = {100,100,200,300};
canvas->drawOval(rect, paint);
```

<img width="400" alt="image" src="https://github.com/user-attachments/assets/2b05bd00-10d3-42b7-8cd8-10d42223ccce" />



# Apis

* drawColor
* clear
* drawPoint
* drawPaint
* drawLine
