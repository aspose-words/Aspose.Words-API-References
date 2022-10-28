---
title: aspect_ratio_locked property
second_title: Aspose.Words for Python via .NET API Reference
description: "Specifies whether the shape's aspect ratio is locked."
type: docs
weight: 40
url: /python-net/aspose.words.drawing/shapebase/aspect_ratio_locked/
---

## ShapeBase.aspect_ratio_locked property

Specifies whether the shape's aspect ratio is locked.

The default value depends on the [ShapeType](../../shapetype/), for the [ShapeType.IMAGE](../../shapetype/#IMAGE) it is ``True``
but for the other shape types it is ``False``.

Has effect for top level shapes only.




### Examples

Shows how to lock/unlock a shape's aspect ratio.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Insert a shape. If we open this document in Microsoft Word, we can left click the shape to reveal
# eight sizing handles around its perimeter, which we can click and drag to change its size.
shape = builder.insert_image(IMAGE_DIR + "Logo.jpg")

# Set the "aspect_ratio_locked" property to "True" to preserve the shape's aspect ratio
# when using any of the four diagonal sizing handles, which change both the image's height and width.
# Using any orthogonal sizing handles that either change the height or width will still change the aspect ratio.
# Set the "aspect_ratio_locked" property to "False" to allow us to
# freely change the image's aspect ratio with all sizing handles.
shape.aspect_ratio_locked = lock_aspect_ratio

doc.save(ARTIFACTS_DIR + "Shape.aspect_ratio.docx")
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

