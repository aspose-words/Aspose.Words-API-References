﻿---
title: ShapeBase.distance_top property
linktitle: distance_top property
articleTitle: distance_top property
second_title: Aspose.Words for Python
description: "ShapeBase.distance_top property. Returns or sets the distance (in points) between the document text and the top edge of the shape."
type: docs
weight: 160
url: /python-net/aspose.words.drawing/shapebase/distance_top/
---

## ShapeBase.distance_top property

Returns or sets the distance (in points) between the document text and the top edge of the shape.


```python
@property
def distance_top(self) -> float:
    ...

@distance_top.setter
def distance_top(self, value: float):
    ...

```

### Remarks

The default value is 0.

Has effect only for top level shapes.




### Examples

Shows how to set the wrapping distance for a text that surrounds a shape.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Insert a rectangle and, get the text to wrap tightly around its bounds.
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, width=150, height=150)
shape.wrap_type = aw.drawing.WrapType.TIGHT
# Set the minimum distance between the shape and surrounding text to 40pt from all sides.
shape.distance_top = 40
shape.distance_bottom = 40
shape.distance_left = 40
shape.distance_right = 40
# Move the shape closer to the center of the page, and then rotate the shape 60 degrees clockwise.
shape.top = 75
shape.left = 150
shape.rotation = 60
# Add text that will wrap around the shape.
builder.font.size = 24
builder.write('Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ' + 'Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.')
doc.save(file_name=ARTIFACTS_DIR + 'Shape.Coordinates.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

