---
title: ShapeBase.is_inline property
linktitle: is_inline property
articleTitle: is_inline property
second_title: Aspose.Words for Python
description: "ShapeBase.is_inline property. A quick way to determine if this shape is positioned inline with text."
type: docs
weight: 310
url: /it/python-net/aspose.words.drawing/shapebase/is_inline/
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
builder = aw.DocumentBuilder(doc=doc)
# Di seguito sono riportati due tipi di avvolgimento che le forme possono avere.
# 1 -  Inline:
builder.write('Hello world! ')
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, width=100, height=100)
shape.fill_color = aspose.pydrawing.Color.light_blue
builder.write(' Hello again.')
# Una forma inline si trova all'interno di un paragrafo tra gli altri elementi del paragrafo, come sequenze di testo.
# In Microsoft Word, possiamo fare clic e trascinare la forma in qualsiasi paragrafo come se fosse un carattere.
# Se la forma è grande, influenzerà la spaziatura verticale del paragrafo.
# Non possiamo spostare questa forma in un punto senza paragrafo.
self.assertEqual(aw.drawing.WrapType.INLINE, shape.wrap_type)
self.assertTrue(shape.is_inline)
# 2 -  Floating:
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, horz_pos=aw.drawing.RelativeHorizontalPosition.LEFT_MARGIN, left=200, vert_pos=aw.drawing.RelativeVerticalPosition.TOP_MARGIN, top=200, width=100, height=100, wrap_type=aw.drawing.WrapType.NONE)
shape.fill_color = aspose.pydrawing.Color.orange
# Una forma flottante appartiene al paragrafo in cui la inseriamo,
# che possiamo determinare tramite un simbolo di ancoraggio che appare quando facciamo clic sulla forma.
# Se la forma non ha un simbolo di ancoraggio visibile a sinistra,
# dovremo abilitare gli ancoraggi visibili tramite "Options" -> "Display" -> "Object Anchors".
# In Microsoft Word, possiamo fare clic sinistro e trascinare liberamente questa forma in qualsiasi posizione.
self.assertEqual(aw.drawing.WrapType.NONE, shape.wrap_type)
self.assertFalse(shape.is_inline)
doc.save(file_name=ARTIFACTS_DIR + 'Shape.IsInline.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

