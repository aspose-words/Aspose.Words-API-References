---
title: ShapeBase.is_inline property
linktitle: is_inline property
articleTitle: is_inline property
second_title: Aspose.Words for Python
description: "ShapeBase.is_inline property. A quick way to determine if this shape is positioned inline with text."
type: docs
weight: 290
url: /python-net/aspose.words.drawing/shapebase/is_inline/
---

## ShapeBase.is_inline property

A quick way to determine if this shape is positioned inline with text.


```python
@property
def is_inline(self) -> bool:
    ...

```

### Remarks

Has effect only for top level shapes.




### Examples

Shows how to determine whether a shape is inline or floating.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Below are two wrapping types that shapes may have.
# 1 -  Inline:
builder.write("Hello world! ")
shape = builder.insert_shape(aw.drawing.ShapeType.RECTANGLE, 100, 100)
shape.fill_color = drawing.Color.light_blue
builder.write(" Hello again.")

# An inline shape sits inside a paragraph among other paragraph elements, such as runs of text.
# In Microsoft Word, we may click and drag the shape to any paragraph as if it is a character.
# If the shape is large, it will affect vertical paragraph spacing.
# We cannot move this shape to a place with no paragraph.
self.assertEqual(aw.drawing.WrapType.INLINE, shape.wrap_type)
self.assertTrue(shape.is_inline)

# 2 -  Floating:
shape = builder.insert_shape(aw.drawing.ShapeType.RECTANGLE, aw.drawing.RelativeHorizontalPosition.LEFT_MARGIN ,200,
    aw.drawing.RelativeVerticalPosition.TOP_MARGIN ,200, 100, 100, aw.drawing.WrapType.NONE)
shape.fill_color = drawing.Color.orange

# A floating shape belongs to the paragraph that we insert it into,
# which we can determine by an anchor symbol that appears when we click the shape.
# If the shape does not have a visible anchor symbol to its left,
# we will need to enable visible anchors via "Options" -> "Display" -> "Object Anchors".
# In Microsoft Word, we may left click and drag this shape freely to any location.
self.assertEqual(aw.drawing.WrapType.NONE, shape.wrap_type)
self.assertFalse(shape.is_inline)

doc.save(ARTIFACTS_DIR + "Shape.is_inline.docx")
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

