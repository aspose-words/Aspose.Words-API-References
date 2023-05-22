---
title: ShapeBase.markup_language property
linktitle: markup_language property
articleTitle: markup_language property
second_title: Aspose.Words for Python
description: "ShapeBase.markup_language property. Gets MarkupLanguage used for this graphic object."
type: docs
weight: 390
url: /python-net/aspose.words.drawing/shapebase/markup_language/
---

## ShapeBase.markup_language property

Gets MarkupLanguage used for this graphic object.


### Examples

Shows how to verify a shape's size and markup language.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

shape = builder.insert_image(IMAGE_DIR + "Transparent background logo.png")

self.assertEqual(aw.drawing.ShapeMarkupLanguage.DML, shape.markup_language)
self.assertEqual(drawing.SizeF(300, 300), shape.size_in_points)
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

