---
title: ShapeBase.is_top_level property
linktitle: is_top_level property
articleTitle: is_top_level property
second_title: Aspose.Words for Python
description: "ShapeBase.is_top_level property. Returns ``True`` if this shape is not a child of a group shape."
type: docs
weight: 370
url: /es/python-net/aspose.words.drawing/shapebase/is_top_level/
---

## ShapeBase.is_top_level property

Returns ``True`` if this shape is not a child of a group shape.



```python
@property
def is_top_level(self) -> bool:
    ...

```

### Examples

Shows how to tell whether a shape is a part of a group shape.

```python
doc = aw.Document()
shape = aw.drawing.Shape(doc, aw.drawing.ShapeType.RECTANGLE)
shape.width = 200
shape.height = 200
shape.wrap_type = aw.drawing.WrapType.NONE
# Una forma por defecto no forma parte de ningún grupo de formas, y por lo tanto tiene la propiedad "IsTopLevel" establecida en "true".
self.assertTrue(shape.is_top_level)
group = aw.drawing.GroupShape(doc)
group.append_child(shape)
# Una vez que incorporamos una forma en un grupo de formas, la propiedad "IsTopLevel" cambia a "false".
self.assertFalse(shape.is_top_level)
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

