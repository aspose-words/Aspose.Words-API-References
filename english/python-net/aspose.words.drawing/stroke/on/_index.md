---
title: on property
second_title: Aspose.Words for Python via .NET API Reference
description: "Defines whether the path will be stroked."
type: docs
weight: 130
url: /python-net/aspose.words.drawing/stroke/on/
---

## Stroke.on property

Defines whether the path will be stroked.

The default value for a [Shape](../../shape/) is **true**.




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

doc.save(ARTIFACTS_DIR + "Shape.stroke.docx")
```

### See Also

* module [aspose.words.drawing](../../)
* class [Stroke](../)

