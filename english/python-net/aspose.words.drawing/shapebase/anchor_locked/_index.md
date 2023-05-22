---
title: ShapeBase.anchor_locked property
linktitle: anchor_locked property
articleTitle: anchor_locked property
second_title: Aspose.Words for Python
description: "ShapeBase.anchor_locked property. Specifies whether the shape's anchor is locked."
type: docs
weight: 30
url: /python-net/aspose.words.drawing/shapebase/anchor_locked/
---

## ShapeBase.anchor_locked property

Specifies whether the shape's anchor is locked.

The default value is ``False``.

Has effect only for top level shapes.

This property affects behavior of the shape's anchor in Microsoft Word.
When the anchor is not locked, moving the shape in Microsoft Word can move
the shape's anchor too.




### Examples

Shows how to lock or unlock a shape's paragraph anchor.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.writeln("Hello world!")

builder.write("Our shape will have an anchor attached to this paragraph.")
shape = builder.insert_shape(aw.drawing.ShapeType.RECTANGLE, 200, 160)
shape.wrap_type = aw.drawing.WrapType.NONE
builder.insert_break(aw.BreakType.PARAGRAPH_BREAK)

builder.writeln("Hello again!")

# Set the "anchor_locked" property to "True" to prevent the shape's anchor
# from moving when moving the shape in Microsoft Word.
# Set the "anchor_locked" property to "False" to allow any movement of the shape
# to also move its anchor to any other paragraph that the shape ends up close to.
shape.anchor_locked = anchor_locked

# If the shape does not have a visible anchor symbol to its left,
# we will need to enable visible anchors via "Options" -> "Display" -> "Object Anchors".
doc.save(ARTIFACTS_DIR + "Shape.anchor_locked.docx")
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

