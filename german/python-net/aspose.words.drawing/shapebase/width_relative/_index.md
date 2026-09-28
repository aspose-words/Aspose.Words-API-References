---
title: ShapeBase.width_relative property
linktitle: width_relative property
articleTitle: width_relative property
second_title: Aspose.Words for Python
description: "ShapeBase.width_relative property. Gets or sets the value that represents the percentage of shape's relative width."
type: docs
weight: 620
url: /de/python-net/aspose.words.drawing/shapebase/width_relative/
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
# Hinzufügen einer einfachen Form mit absoluter Größe und Position.
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, width=100, height=40)
# Setzen Sie WrapType auf WrapType.None, da Inline-Formen automatisch in absolute Einheiten konvertiert werden.
shape.wrap_type = aw.drawing.WrapType.NONE
# Überprüfen und Festlegen der relativen horizontalen Größe.
if shape.relative_horizontal_size == aw.drawing.RelativeHorizontalSize.DEFAULT:
    # Festlegen der Bindung der horizontalen Größe an den Rand.
    shape.relative_horizontal_size = aw.drawing.RelativeHorizontalSize.MARGIN
    # Festlegen der Breite auf 50 % der Randbreite.
    shape.width_relative = 50
# Überprüfen und Festlegen der relativen vertikalen Größe.
if shape.relative_vertical_size == aw.drawing.RelativeVerticalSize.DEFAULT:
    # Festlegen der Bindung der vertikalen Größe an den Rand.
    shape.relative_vertical_size = aw.drawing.RelativeVerticalSize.MARGIN
    # Festlegen der Höhe auf 30 % der Randhöhe.
    shape.height_relative = 30
# Überprüfen und Festlegen der relativen vertikalen Position.
if shape.relative_vertical_position == aw.drawing.RelativeVerticalPosition.PARAGRAPH:
    # Festlegen der Positionsbindung an TopMargin.
    shape.relative_vertical_position = aw.drawing.RelativeVerticalPosition.TOP_MARGIN
    # Relative Oberkante auf 30 % der TopMargin-Position festlegen.
    shape.top_relative = 30
# Überprüfen und Festlegen der relativen horizontalen Position.
if shape.relative_horizontal_position == aw.drawing.RelativeHorizontalPosition.DEFAULT:
    # Festlegen der Positionsbindung an RightMargin.
    shape.relative_horizontal_position = aw.drawing.RelativeHorizontalPosition.RIGHT_MARGIN
    # Der relative Positionswert kann negativ sein.
    shape.left_relative = -260
doc.save(file_name=ARTIFACTS_DIR + 'Shape.RelativeSizeAndPosition.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

