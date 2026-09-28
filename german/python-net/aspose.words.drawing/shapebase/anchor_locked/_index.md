---
title: ShapeBase.anchor_locked property
linktitle: anchor_locked property
articleTitle: anchor_locked property
second_title: Aspose.Words for Python
description: "ShapeBase.anchor_locked property. Specifies whether the shape's anchor is locked."
type: docs
weight: 30
url: /de/python-net/aspose.words.drawing/shapebase/anchor_locked/
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
# Setzen Sie die Eigenschaft "AnchorLocked" auf "true", um den Anker der Form
# vor dem Verschieben zu schützen, wenn die Form in Microsoft Word bewegt wird.
# Setzen Sie die Eigenschaft "AnchorLocked" auf "false", um jede Bewegung der Form zu ermöglichen
# und ihren Anker ebenfalls zu einem anderen Absatz zu verschieben, dem die Form nahe kommt.
shape.anchor_locked = anchor_locked
# Wenn die Form kein sichtbares Ankersymbol zu ihrer linken Seite hat,
# müssen wir sichtbare Anker über "Options" -> "Display" -> "Object Anchors" aktivieren.
doc.save(file_name=ARTIFACTS_DIR + 'Shape.AnchorLocked.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

