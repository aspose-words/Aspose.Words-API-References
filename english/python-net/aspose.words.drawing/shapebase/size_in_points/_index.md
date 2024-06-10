---
title: ShapeBase.size_in_points property
linktitle: size_in_points property
articleTitle: size_in_points property
second_title: Aspose.Words for Python
description: "ShapeBase.size_in_points property. Gets the size of the shape in points."
type: docs
weight: 530
url: /python-net/aspose.words.drawing/shapebase/size_in_points/
---

## ShapeBase.size_in_points property

Gets the size of the shape in points.


```python
@property
def size_in_points(self) -> aspose.pydrawing.SizeF:
    ...

```

### Examples

Shows how to verify a shape's size and markup language.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
shape = builder.insert_image(file_name=IMAGE_DIR + 'Transparent background logo.png')
self.assertEqual(aw.drawing.ShapeMarkupLanguage.DML, shape.markup_language)
self.assertEqual(aspose.pydrawing.SizeF(300, 300), shape.size_in_points)
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

