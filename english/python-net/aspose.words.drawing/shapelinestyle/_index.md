---
title: ShapeLineStyle enumeration
linktitle: ShapeLineStyle enumeration
articleTitle: ShapeLineStyle enumeration
second_title: Aspose.Words for Python
description: "aspose.words.drawing.ShapeLineStyle enumeration. Specifies the compound line style of a [Shape](../shape/)."
type: docs
weight: 340
url: /python-net/aspose.words.drawing/shapelinestyle/
---

## ShapeLineStyle enumeration

Specifies the compound line style of a [Shape](../shape/).



### Members

| Name | Description |
| --- | --- |
| SINGLE | Single line. |
| DOUBLE | Double lines of equal width. |
| THICK_THIN | Double lines, one thick, one thin. |
| THIN_THICK | Double lines, one thin, one thick. |
| TRIPLE | Three lines, thin, thick, thin. |
| DEFAULT | Default value is [ShapeLineStyle.SINGLE](./#SINGLE). |

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

* module [aspose.words.drawing](../)
* property [Stroke.line_style](../stroke/line_style/)

