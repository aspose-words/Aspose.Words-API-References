﻿---
title: DashStyle enumeration
second_title: Aspose.Words for Python via .NET API Reference
description: "Dashed line style."
type: docs
weight: 40
url: /python-net/aspose.words.drawing/dashstyle/
---

## DashStyle enumeration

Dashed line style.


### Members

| Name | Description |
| --- | --- |
| SOLID | Solid (continuous) pen. |
| SHORT_DASH | System dash style. |
| SHORT_DOT | System dash style. |
| SHORT_DASH_DOT | System dash style. |
| SHORT_DASH_DOT_DOT | System dash style. |
| DOT | Square dot style. |
| DASH | Dash style. |
| LONG_DASH | Long dash style. |
| DASH_DOT | Dash short dash. |
| LONG_DASH_DOT | Long dash short dash. |
| LONG_DASH_DOT_DOT | Long dash short dash short dash. |
| DEFAULT | Same as [DashStyle.SOLID](./#SOLID). |

### Examples

Shows to create a variety of shapes.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Below are four examples of shapes that we can insert into our documents.
# 1 -  Dotted, horizontal, half-transparent red line
# with an arrow on the left end and a diamond on the right end:
arrow = aw.drawing.Shape(doc, aw.drawing.ShapeType.LINE)
arrow.width = 200
arrow.stroke.color = drawing.Color.red
arrow.stroke.start_arrow_type = aw.drawing.ArrowType.ARROW
arrow.stroke.start_arrow_length = aw.drawing.ArrowLength.LONG
arrow.stroke.start_arrow_width = aw.drawing.ArrowWidth.WIDE
arrow.stroke.end_arrow_type = aw.drawing.ArrowType.DIAMOND
arrow.stroke.end_arrow_length = aw.drawing.ArrowLength.LONG
arrow.stroke.end_arrow_width = aw.drawing.ArrowWidth.WIDE
arrow.stroke.dash_style = aw.drawing.DashStyle.DASH
arrow.stroke.opacity = 0.5

self.assertEqual(aw.drawing.JoinStyle.MITER, arrow.stroke.join_style)

builder.insert_node(arrow)

# 2 -  Thick black diagonal line with rounded ends:
line = aw.drawing.Shape(doc, aw.drawing.ShapeType.LINE)
line.top = 40
line.width = 200
line.height = 20
line.stroke_weight = 5.0
line.stroke.end_cap = aw.drawing.EndCap.ROUND

builder.insert_node(line)

# 3 -  Arrow with a green fill:
filled_in_arrow = aw.drawing.Shape(doc, aw.drawing.ShapeType.ARROW)
filled_in_arrow.width = 200
filled_in_arrow.height = 40
filled_in_arrow.top = 100
filled_in_arrow.fill.fore_color = drawing.Color.green
filled_in_arrow.fill.visible = True

builder.insert_node(filled_in_arrow)

# 4 -  Arrow with a flipped orientation filled in with the Aspose logo:
filled_in_arrow_img = aw.drawing.Shape(doc, aw.drawing.ShapeType.ARROW)
filled_in_arrow_img.width = 200
filled_in_arrow_img.height = 40
filled_in_arrow_img.top = 160
filled_in_arrow_img.flip_orientation = aw.drawing.FlipOrientation.BOTH

with open(IMAGE_DIR + "Logo.jpg", "rb") as stream:

    image = drawing.Image.from_stream(stream)
    # When we flip the orientation of our arrow, we also flip the image that the arrow contains.
    # Flip the image the other way to cancel this out before getting the shape to display it.
    image.rotate_flip(drawing.RotateFlipType.ROTATE_NONE_FLIP_XY)

    filled_in_arrow_img.image_data.set_image(image)
    filled_in_arrow_img.stroke.join_style = aw.drawing.JoinStyle.ROUND

    builder.insert_node(filled_in_arrow_img)

doc.save(ARTIFACTS_DIR + "Drawing.various_shapes.docx")
```

### See Also

* module [aspose.words.drawing](../)
* property [Stroke.dash_style](../stroke/dash_style/)
