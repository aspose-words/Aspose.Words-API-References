﻿---
title: Stroke class
linktitle: Stroke class
articleTitle: Stroke class
second_title: Aspose.Words for Python
description: "aspose.words.drawing.Stroke class. Defines a stroke for a shape"
type: docs
weight: 440
url: /python-net/aspose.words.drawing/stroke/
---

## Stroke class

Defines a stroke for a shape.
To learn more, visit the [Working with Shapes](https://docs.aspose.com/words/python-net/working-with-shapes/) documentation article.




### Remarks

Use the [Shape.stroke](../shape/stroke/) property to access stroke properties of a shape.
You do not create instances of the [Stroke](./) class directly.




### Properties

| Name | Description |
| --- | --- |
| [back_color](./back_color/) | Gets or sets the background color of the stroke. |
| [back_theme_color](./back_theme_color/) | Gets or sets a ThemeColor object that represents the stroke background color. |
| [back_tint_and_shade](./back_tint_and_shade/) | Gets or sets a double value that lightens or darkens the stroke background color. |
| [base_fore_color](./base_fore_color/) | Gets the base foreground color of the stroke without any modifiers. |
| [color](./color/) | Defines the color of a stroke. |
| [color2](./color2/) | Defines a second color for a stroke. |
| [dash_style](./dash_style/) | Specifies the dot and dash pattern for a stroke. |
| [end_arrow_length](./end_arrow_length/) | Defines the arrowhead length for the end of a stroke. |
| [end_arrow_type](./end_arrow_type/) | Defines the arrowhead for the end of a stroke. |
| [end_arrow_width](./end_arrow_width/) | Defines the arrowhead width for the end of a stroke. |
| [end_cap](./end_cap/) | Defines the cap style for the end of a stroke. |
| [fill](./fill/) | Gets fill formatting for the [Stroke](./). |
| [fore_color](./fore_color/) | Gets or sets the foreground color of the stroke. |
| [fore_theme_color](./fore_theme_color/) | Gets or sets a ThemeColor object that represents the stroke foreground color. |
| [fore_tint_and_shade](./fore_tint_and_shade/) | Gets or sets a double value that lightens or darkens the stroke foreground color. |
| [image_bytes](./image_bytes/) | Defines the image for a stroke image or pattern fill. |
| [join_style](./join_style/) | Defines the join style of a polyline. |
| [line_style](./line_style/) | Defines the line style of the stroke. |
| [on](./on/) | Defines whether the path will be stroked. |
| [opacity](./opacity/) | Defines the amount of transparency of a stroke. Valid range is from 0 to 1. |
| [start_arrow_length](./start_arrow_length/) | Defines the arrowhead length for the start of a stroke. |
| [start_arrow_type](./start_arrow_type/) | Defines the arrowhead for the start of a stroke. |
| [start_arrow_width](./start_arrow_width/) | Defines the arrowhead width for the start of a stroke. |
| [transparency](./transparency/) | Gets or sets a value between 0.0 (opaque) and 1.0 (clear) representing the degree of transparency of the stroke. |
| [visible](./visible/) | Gets or sets a flag indicating whether the stroke is visible. |
| [weight](./weight/) | Defines the brush thickness that strokes the path of a shape in points. |

### Examples

Shows how change stroke properties.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
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

* module [aspose.words.drawing](../)
* property [Shape.stroke](../shape/stroke/)

