---
title: ShapeBase.anchor_locked property
linktitle: anchor_locked property
articleTitle: anchor_locked property
second_title: Aspose.Words for Python
description: "ShapeBase.anchor_locked property. Specifies whether the shape's anchor is locked."
type: docs
weight: 30
url: /tr/python-net/aspose.words.drawing/shapebase/anchor_locked/
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
# \"AnchorLocked\" özelliğini \"true\" olarak ayarlayın, böylece şeklin ankrajı
# Microsoft Word'de şekli hareket ettirirken hareket etmesini önleyin.
# \"AnchorLocked\" özelliğini \"false\" olarak ayarlayın, böylece şeklin herhangi bir hareketine izin verilir
# ve ankrajını şeklin yaklaştığı herhangi bir başka paragrafa da taşıyabilir.
shape.anchor_locked = anchor_locked
# Şeklin solunda görünür bir çapa simgesi yoksa,
# görünür çapaları "Options" -> "Display" -> "Object Anchors" üzerinden etkinleştirmemiz gerekir.
doc.save(file_name=ARTIFACTS_DIR + 'Shape.AnchorLocked.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

