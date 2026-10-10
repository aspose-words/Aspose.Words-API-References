---
title: ShapeBase.anchor_locked property
linktitle: anchor_locked property
articleTitle: anchor_locked property
second_title: Aspose.Words for Python
description: "ShapeBase.anchor_locked property. Specifies whether the shape's anchor is locked."
type: docs
weight: 30
url: /ru/python-net/aspose.words.drawing/shapebase/anchor_locked/
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
# Установите свойство "AnchorLocked" в значение "true", чтобы предотвратить привязку фигуры
# от перемещения при перемещении фигуры в Microsoft Word.
# Установите свойство "AnchorLocked" в значение "false", чтобы разрешить любое перемещение фигуры
# а также перемещать её привязку к любому другому абзацу, к которому фигура окажется близко.
shape.anchor_locked = anchor_locked
# Если у фигуры слева нет видимого символа якоря,
# нам понадобится включить видимые якоря через "Options" -> "Display" -> "Object Anchors".
doc.save(file_name=ARTIFACTS_DIR + 'Shape.AnchorLocked.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

