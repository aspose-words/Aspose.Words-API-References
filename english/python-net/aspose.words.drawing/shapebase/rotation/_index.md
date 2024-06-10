---
title: ShapeBase.rotation property
linktitle: rotation property
articleTitle: rotation property
second_title: Aspose.Words for Python
description: "ShapeBase.rotation property. Defines the angle (in degrees) that a shape is rotated"
type: docs
weight: 490
url: /python-net/aspose.words.drawing/shapebase/rotation/
---

## ShapeBase.rotation property

Defines the angle (in degrees) that a shape is rotated.
Positive value corresponds to clockwise rotation angle.


```python
@property
def rotation(self) -> float:
    ...

@rotation.setter
def rotation(self, value: float):
    ...

```

### Remarks

The default value is 0.




### Examples

Shows how to insert and rotate an image.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
# Insert a shape with an image.
shape = builder.insert_image(drawing.Image.from_file(IMAGE_DIR + 'Logo.jpg'))
self.assertTrue(shape.can_have_image)
self.assertTrue(shape.has_image)
# Rotate the image 45 degrees clockwise.
shape.rotation = 45
doc.save(ARTIFACTS_DIR + 'Shape.rotate.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

