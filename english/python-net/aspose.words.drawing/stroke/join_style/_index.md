---
title: Stroke.join_style property
linktitle: join_style property
articleTitle: join_style property
second_title: Aspose.Words for Python
description: "Stroke.join_style property. Defines the join style of a polyline."
type: docs
weight: 170
url: /python-net/aspose.words.drawing/stroke/join_style/
---

## Stroke.join_style property

Defines the join style of a polyline.


```python
@property
def join_style(self) -> aspose.words.drawing.JoinStyle:
    ...

@join_style.setter
def join_style(self, value: aspose.words.drawing.JoinStyle):
    ...

```

### Remarks

The default value is [JoinStyle.ROUND](../../joinstyle/#ROUND).




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

