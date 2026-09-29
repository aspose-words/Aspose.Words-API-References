---
title: ShapeBase.width_relative property
linktitle: width_relative property
articleTitle: width_relative property
second_title: Aspose.Words for Python
description: "ShapeBase.width_relative property. Gets or sets the value that represents the percentage of shape's relative width."
type: docs
weight: 620
url: /sv/python-net/aspose.words.drawing/shapebase/width_relative/
---

## ShapeBase.width_relative property

Gets or sets the value that represents the percentage of shape's relative width.


```python
@property
def width_relative(self) -> float:
    ...

@width_relative.setter
def width_relative(self, value: float):
    ...

```

### Examples

Shows how to set relative size and position.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Lägger till en enkel form med absolut storlek och position.
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, width=100, height=40)
# Ställ in WrapType till WrapType.None eftersom inline‑former automatiskt konverteras till absoluta enheter.
shape.wrap_type = aw.drawing.WrapType.NONE
# Kontrollerar och ställer in relativ horisontell storlek.
if shape.relative_horizontal_size == aw.drawing.RelativeHorizontalSize.DEFAULT:
    # Ställer in horisontell storleksbindning till Margin.
    shape.relative_horizontal_size = aw.drawing.RelativeHorizontalSize.MARGIN
    # Ställer in bredden till 50 % av Marginalens bredd.
    shape.width_relative = 50
# Kontrollerar och ställer in relativ vertikal storlek.
if shape.relative_vertical_size == aw.drawing.RelativeVerticalSize.DEFAULT:
    # Ställer in vertikal storleksbindning till Margin.
    shape.relative_vertical_size = aw.drawing.RelativeVerticalSize.MARGIN
    # Ställer in höjden till 30 % av Marginalens höjd.
    shape.height_relative = 30
# Kontrollerar och ställer in relativ vertikal position.
if shape.relative_vertical_position == aw.drawing.RelativeVerticalPosition.PARAGRAPH:
    # Ställer in positionsbindning till TopMargin.
    shape.relative_vertical_position = aw.drawing.RelativeVerticalPosition.TOP_MARGIN
    # Ställer in relativ topp till 30 % av TopMargin‑positionen.
    shape.top_relative = 30
# Kontrollerar och ställer in relativ horisontell position.
if shape.relative_horizontal_position == aw.drawing.RelativeHorizontalPosition.DEFAULT:
    # Ställer in positionsbindning till RightMargin.
    shape.relative_horizontal_position = aw.drawing.RelativeHorizontalPosition.RIGHT_MARGIN
    # Det relativa positionsvärdet kan vara negativt.
    shape.left_relative = -260
doc.save(file_name=ARTIFACTS_DIR + 'Shape.RelativeSizeAndPosition.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

