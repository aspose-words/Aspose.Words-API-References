---
title: can_have_image property
second_title: Aspose.Words for Python via .NET API Reference
description: "Returns true if the shape type allows the shape to have an image."
type: docs
weight: 100
url: /python-net/aspose.words.drawing/shapebase/can_have_image/
---

## ShapeBase.can_have_image property

Returns true if the shape type allows the shape to have an image.

Although Microsoft Word has a special shape type for images, it appears that in Microsoft Word documents any shape
except a group shape can have an image, therefore this property returns true for all shapes except [GroupShape](../../groupshape/).




### Examples

Shows how to insert and rotate an image.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Insert a shape with an image.
shape = builder.insert_image(drawing.Image.from_file(IMAGE_DIR + "Logo.jpg"))
self.assertTrue(shape.can_have_image)
self.assertTrue(shape.has_image)

# Rotate the image 45 degrees clockwise.
shape.rotation = 45

doc.save(ARTIFACTS_DIR + "Shape.rotate.docx")
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

