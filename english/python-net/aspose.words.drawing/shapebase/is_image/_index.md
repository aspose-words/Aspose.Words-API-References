---
title: ShapeBase.is_image property
linktitle: is_image property
articleTitle: is_image property
second_title: Aspose.Words for Python
description: "ShapeBase.is_image property. Returns ``True`` if this shape is an image shape."
type: docs
weight: 300
url: /python-net/aspose.words.drawing/shapebase/is_image/
---

## ShapeBase.is_image property

Returns ``True`` if this shape is an image shape.



```python
@property
def is_image(self) -> bool:
    ...

```

### Examples

Shows how to open an HTML document with images from a stream using a base URI.

```python
with system_helper.io.File.open_read(MY_DIR + 'Document.html') as stream:
    # Pass the URI of the base folder while loading it
    # so that any images with relative URIs in the HTML document can be found.
    load_options = aw.loading.LoadOptions()
    load_options.base_uri = IMAGE_DIR
    doc = aw.Document(stream=stream, load_options=load_options)
    # Verify that the first shape of the document contains a valid image.
    shape = doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape()
    self.assertTrue(shape.is_image)
    self.assertIsNotNone(shape.image_data.image_bytes)
    self.assertAlmostEqual(32, aw.ConvertUtil.point_to_pixel(points=shape.width), delta=0.01)
    self.assertAlmostEqual(32, aw.ConvertUtil.point_to_pixel(points=shape.height), delta=0.01)
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

