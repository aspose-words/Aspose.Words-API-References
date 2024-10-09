---
title: ShapeBase.markup_language property
linktitle: markup_language property
articleTitle: markup_language property
second_title: Aspose.Words for Python
description: "ShapeBase.markup_language property. Gets MarkupLanguage used for this graphic object."
type: docs
weight: 410
url: /python-net/aspose.words.drawing/shapebase/markup_language/
---

## ShapeBase.markup_language property

Gets MarkupLanguage used for this graphic object.


```python
@property
def markup_language(self) -> aspose.words.drawing.ShapeMarkupLanguage:
    ...

```

### Examples

Shows how to verify a shape's size and markup language.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_image(file_name=IMAGE_DIR + 'Transparent background logo.png')
self.assertEqual(aw.drawing.ShapeMarkupLanguage.DML, shape.markup_language)
self.assertEqual(aspose.pydrawing.SizeF(300, 300), shape.size_in_points)
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

