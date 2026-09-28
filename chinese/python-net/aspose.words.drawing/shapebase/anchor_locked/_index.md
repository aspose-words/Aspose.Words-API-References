---
title: ShapeBase.anchor_locked property
linktitle: anchor_locked property
articleTitle: anchor_locked property
second_title: Aspose.Words for Python
description: "ShapeBase.anchor_locked property. Specifies whether the shape's anchor is locked."
type: docs
weight: 30
url: /zh/python-net/aspose.words.drawing/shapebase/anchor_locked/
---

## ShapeBase.anchor_locked property

Specifies whether the shape's anchor is locked.


```python
@property
def anchor_locked(self) -> bool:
    ...

@anchor_locked.setter
def anchor_locked(self, value: bool):
    ...

```

### Remarks

The default value is ``False``.

Has effect only for top level shapes.

This property affects behavior of the shape's anchor in Microsoft Word.
When the anchor is not locked, moving the shape in Microsoft Word can move
the shape's anchor too.




### Examples

Shows how to lock or unlock a shape's paragraph anchor.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Hello world!')
builder.write('Our shape will have an anchor attached to this paragraph.')
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, width=200, height=160)
shape.wrap_type = aw.drawing.WrapType.NONE
builder.insert_break(aw.BreakType.PARAGRAPH_BREAK)
builder.writeln('Hello again!')
# 将 "AnchorLocked" 属性设置为 "true"，以防止形状的锚点
# 在 Microsoft Word 中移动形状时防止锚点移动。
# 将 "AnchorLocked" 属性设置为 "false"，以允许形状的任何移动
# 并将其锚点移动到形状最终靠近的任何其他段落。
shape.anchor_locked = anchor_locked
# 如果形状左侧没有可见的锚点符号，
# 我们需要通过 "Options" -> "Display" -> "Object Anchors" 来启用可见锚点。
doc.save(file_name=ARTIFACTS_DIR + 'Shape.AnchorLocked.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

