---
title: RelativeVerticalSize enumeration
linktitle: RelativeVerticalSize enumeration
articleTitle: RelativeVerticalSize enumeration
second_title: Aspose.Words for Python
description: "aspose.words.drawing.RelativeVerticalSize enumeration. Specifies relatively to what the height of a shape or a text frame is calculated vertically."
type: docs
weight: 330
url: /de/python-net/aspose.words.drawing/relativeverticalsize/
---

## RelativeVerticalSize enumeration

Specifies relatively to what the height of a shape or a text frame is calculated vertically.


### Members

| Name | Description |
| --- | --- |
| MARGIN | Specifies that the height is calculated relatively to the space between the top and the bottom margins. |
| PAGE | Specifies that the height is calculated relatively to the page height. |
| TOP_MARGIN | Specifies that the height is calculated relatively to the top margin area size. |
| BOTTOM_MARGIN | Specifies that the height is calculated relatively to the bottom margin area size. |
| INNER_MARGIN | Specifies that the height is calculated relatively to the inside margin area size, to the top margin area size for odd pages and to the bottom margin area size for even pages. |
| OUTER_MARGIN | Specifies that the height is calculated relatively to the outside margin area size, to the bottom margin area size for odd pages and to the top margin area size for even pages. |
| DEFAULT | Default value is [RelativeVerticalSize.MARGIN](./#MARGIN). |

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
* property [ShapeBase.relative_vertical_size](../shapebase/relative_vertical_size/)

