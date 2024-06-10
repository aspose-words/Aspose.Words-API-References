---
title: Stroke.line_style property
linktitle: line_style property
articleTitle: line_style property
second_title: Aspose.Words for Python
description: "Stroke.line_style property. Defines the line style of the stroke."
type: docs
weight: 180
url: /python-net/aspose.words.drawing/stroke/line_style/
---

## Stroke.line_style property

Defines the line style of the stroke.


```python
@property
def line_style(self) -> aspose.words.drawing.ShapeLineStyle:
    ...

@line_style.setter
def line_style(self, value: aspose.words.drawing.ShapeLineStyle):
    ...

```

### Remarks

The default value is [ShapeLineStyle.SINGLE](../../shapelinestyle/#SINGLE).




### Examples

Shows how change stroke properties.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, horz_pos=aw.drawing.RelativeHorizontalPosition.LEFT_MARGIN, left=100, vert_pos=aw.drawing.RelativeVerticalPosition.TOP_MARGIN, top=100, width=200, height=200, wrap_type=aw.drawing.WrapType.NONE)
# Basic shapes, such as the rectangle, have two visible parts.
# 1 -  The fill, which applies to the area within the outline of the shape:
shape.fill.fore_color = aspose.pydrawing.Color.white
# 2 -  The stroke, which marks the outline of the shape:
# Modify various properties of this shape's stroke.
stroke = shape.stroke
stroke.on = True
stroke.weight = 5
stroke.color = aspose.pydrawing.Color.red
stroke.dash_style = aw.drawing.DashStyle.SHORT_DASH_DOT_DOT
stroke.join_style = aw.drawing.JoinStyle.MITER
stroke.end_cap = aw.drawing.EndCap.SQUARE
stroke.line_style = aw.drawing.ShapeLineStyle.TRIPLE
stroke.fill.two_color_gradient(color1=aspose.pydrawing.Color.red, color2=aspose.pydrawing.Color.blue, style=aw.drawing.GradientStyle.VERTICAL, variant=aw.drawing.GradientVariant.VARIANT1)
doc.save(file_name=ARTIFACTS_DIR + 'Shape.Stroke.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [Stroke](../)

