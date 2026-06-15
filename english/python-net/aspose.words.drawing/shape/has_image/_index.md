---
title: Shape.has_image property
linktitle: has_image property
articleTitle: has_image property
second_title: Aspose.Words for Python
description: "Shape.has_image property. Returns ``True`` if the shape has image bytes or links an image."
type: docs
weight: 90
url: /python-net/aspose.words.drawing/shape/has_image/
---

## Shape.has_image property

Returns ``True`` if the shape has image bytes or links an image.



```python
@property
def has_image(self) -> bool:
    ...

```

### Examples

Shows how to delete all shapes with images from a document.

```python
doc = aw.Document(file_name=MY_DIR + 'Images.docx')
shapes = doc.get_child_nodes(aw.NodeType.SHAPE, True)
self.assertEqual(9, len(list(filter(lambda s: s.has_image, list(filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_shape(), b), list(shapes))))))))
for shape in filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_shape(), b), list(shapes))):
    if shape.has_image:
        shape.remove()
self.assertEqual(0, len(list(filter(lambda s: s.has_image, list(filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_shape(), b), list(shapes))))))))
```

### See Also

* module [aspose.words.drawing](../../)
* class [Shape](../)

