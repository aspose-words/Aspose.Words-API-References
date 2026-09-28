---
title: RelativeHorizontalSize enumeration
linktitle: RelativeHorizontalSize enumeration
articleTitle: RelativeHorizontalSize enumeration
second_title: Aspose.Words for Python
description: "aspose.words.drawing.RelativeHorizontalSize enumeration. Specifies relatively to what the width of a shape or a text frame is calculated horizontally."
type: docs
weight: 310
url: /de/python-net/aspose.words.drawing/relativehorizontalsize/
---

## RelativeHorizontalSize enumeration

Specifies relatively to what the width of a shape or a text frame is calculated horizontally.


### Members

| Name | Description |
| --- | --- |
| MARGIN | Specifies that the width is calculated relatively to the space between the left and the right margins. |
| PAGE | Specifies that the width is calculated relatively to the page width. |
| LEFT_MARGIN | Specifies that the width is calculated relatively to the left margin area size. |
| RIGHT_MARGIN | Specifies that the width is calculated relatively to the right margin area size. |
| INNER_MARGIN | Specifies that the width is calculated relatively to the inside margin area size, to the left margin area size for odd pages and to the right margin area size for even pages. |
| OUTER_MARGIN | Specifies that the width is calculated relatively to the outside margin area size, to the right margin area size for odd pages and to the left margin area size for even pages. |
| DEFAULT | Default value is [RelativeHorizontalSize.MARGIN](./#MARGIN). |

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

* module [aspose.words.drawing](../)
* property [ShapeBase.relative_horizontal_size](../shapebase/relative_horizontal_size/)

