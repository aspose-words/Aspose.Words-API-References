---
title: Stroke.weight property
linktitle: weight property
articleTitle: weight property
second_title: Aspose.Words for Python
description: "Stroke.weight property. Defines the brush thickness that strokes the path of a shape in points."
type: docs
weight: 220
url: /python-net/aspose.words.drawing/stroke/weight/
---

## Stroke.weight property

Defines the brush thickness that strokes the path of a shape in points.

The default value for a [Shape](../../shape/) is 0.75.




### Examples

Shows how change stroke properties.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

shape = builder.insert_shape(aw.drawing.ShapeType.RECTANGLE, aw.drawing.RelativeHorizontalPosition.LEFT_MARGIN, 100,
    aw.drawing.RelativeVerticalPosition.TOP_MARGIN, 100, 200, 200, aw.drawing.WrapType.NONE)

# Basic shapes, such as the rectangle, have two visible parts.
# 1 -  The fill, which applies to the area within the outline of the shape:
shape.fill.fore_color = drawing.Color.white

# 2 -  The stroke, which marks the outline of the shape:
# Modify various properties of this shape's stroke.
stroke = shape.stroke
stroke.on = True
stroke.weight = 5
stroke.color = drawing.Color.red
stroke.dash_style = aw.drawing.DashStyle.SHORT_DASH_DOT_DOT
stroke.join_style = aw.drawing.JoinStyle.MITER
stroke.end_cap = aw.drawing.EndCap.SQUARE
stroke.line_style = aw.drawing.ShapeLineStyle.TRIPLE

stroke.fill.two_color_gradient(drawing.Color.red, drawing.Color.blue, awd.GradientStyle.VERTICAL, awd.GradientVariant.VARIANT1)

doc.save(ARTIFACTS_DIR + "Shape.stroke.docx")
```

### See Also

* module [aspose.words.drawing](../../)
* class [Stroke](../)

