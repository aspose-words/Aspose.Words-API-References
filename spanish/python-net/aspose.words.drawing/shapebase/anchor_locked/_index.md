---
title: ShapeBase.anchor_locked property
linktitle: anchor_locked property
articleTitle: anchor_locked property
second_title: Aspose.Words for Python
description: "ShapeBase.anchor_locked property. Specifies whether the shape's anchor is locked."
type: docs
weight: 30
url: /es/python-net/aspose.words.drawing/shapebase/anchor_locked/
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
# Establezca la propiedad "AnchorLocked" a "true" para evitar que la ancla de la forma
# se mueva al mover la forma en Microsoft Word.
# para permitir cualquier movimiento de la forma
# para también mover su ancla a cualquier otro párrafo al que la forma quede cerca.
shape.anchor_locked = anchor_locked
# Si la forma no tiene un símbolo de ancla visible a su izquierda,
# necesitaremos habilitar anclas visibles mediante "Options" -> "Display" -> "Object Anchors".
doc.save(file_name=ARTIFACTS_DIR + 'Shape.AnchorLocked.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

