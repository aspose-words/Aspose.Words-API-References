---
title: ShapeBase.flip_orientation property
linktitle: flip_orientation property
articleTitle: flip_orientation property
second_title: Aspose.Words for Python
description: "ShapeBase.flip_orientation property. Switches the orientation of a shape."
type: docs
weight: 180
url: /de/python-net/aspose.words.drawing/shapebase/flip_orientation/
---

## ShapeBase.flip_orientation property

Switches the orientation of a shape.


```python
@property
def flip_orientation(self) -> aspose.words.drawing.FlipOrientation:
    ...

@flip_orientation.setter
def flip_orientation(self, value: aspose.words.drawing.FlipOrientation):
    ...

```

### Remarks

The default value is [FlipOrientation.NONE](../../fliporientation/#NONE).




### Examples

Shows how to flip a shape on an axis.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Fügen Sie eine Bildform ein und lassen Sie ihre Ausrichtung im Standardzustand.
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, horz_pos=aw.drawing.RelativeHorizontalPosition.LEFT_MARGIN, left=100, vert_pos=aw.drawing.RelativeVerticalPosition.TOP_MARGIN, top=100, width=100, height=100, wrap_type=aw.drawing.WrapType.NONE)
shape.image_data.set_image(file_name=IMAGE_DIR + 'Logo.jpg')
self.assertEqual(aw.drawing.FlipOrientation.NONE, shape.flip_orientation)
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, horz_pos=aw.drawing.RelativeHorizontalPosition.LEFT_MARGIN, left=250, vert_pos=aw.drawing.RelativeVerticalPosition.TOP_MARGIN, top=100, width=100, height=100, wrap_type=aw.drawing.WrapType.NONE)
shape.image_data.set_image(file_name=IMAGE_DIR + 'Logo.jpg')
# Setzen Sie die "FlipOrientation"-Eigenschaft auf "FlipOrientation.Horizontal", um die zweite Form entlang der y-Achse zu spiegeln,
# und sie zu einem horizontalen Spiegelbild der ersten Form machen.
shape.flip_orientation = aw.drawing.FlipOrientation.HORIZONTAL
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, horz_pos=aw.drawing.RelativeHorizontalPosition.LEFT_MARGIN, left=100, vert_pos=aw.drawing.RelativeVerticalPosition.TOP_MARGIN, top=250, width=100, height=100, wrap_type=aw.drawing.WrapType.NONE)
shape.image_data.set_image(file_name=IMAGE_DIR + 'Logo.jpg')
# Setzen Sie die "FlipOrientation"-Eigenschaft auf "FlipOrientation.Horizontal", um die dritte Form auf der x-Achse zu drehen,
# um sie in ein vertikales Spiegelbild der ersten Form zu verwandeln.
shape.flip_orientation = aw.drawing.FlipOrientation.VERTICAL
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, horz_pos=aw.drawing.RelativeHorizontalPosition.LEFT_MARGIN, left=250, vert_pos=aw.drawing.RelativeVerticalPosition.TOP_MARGIN, top=250, width=100, height=100, wrap_type=aw.drawing.WrapType.NONE)
shape.image_data.set_image(file_name=IMAGE_DIR + 'Logo.jpg')
# Setzen Sie die "FlipOrientation"-Eigenschaft auf "FlipOrientation.Horizontal", um die vierte Form sowohl auf der x- als auch auf der y-Achse zu drehen,
# um sie in ein horizontales und vertikales Spiegelbild der ersten Form zu verwandeln.
shape.flip_orientation = aw.drawing.FlipOrientation.BOTH
doc.save(file_name=ARTIFACTS_DIR + 'Shape.FlipShapeOrientation.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

