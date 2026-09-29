---
title: ShapeBase.is_inline property
linktitle: is_inline property
articleTitle: is_inline property
second_title: Aspose.Words for Python
description: "ShapeBase.is_inline property. A quick way to determine if this shape is positioned inline with text."
type: docs
weight: 310
url: /es/python-net/aspose.words.drawing/shapebase/is_inline/
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
# A continuación se presentan dos tipos de ajuste que pueden tener las formas.
# 1 -  En línea:
builder.write('Hello world! ')
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, width=100, height=100)
shape.fill_color = aspose.pydrawing.Color.light_blue
builder.write(' Hello again.')
# Una forma en línea se sitúa dentro de un párrafo entre otros elementos del párrafo, como secuencias de texto.
# En Microsoft Word, podemos hacer clic y arrastrar la forma a cualquier párrafo como si fuera un carácter.
# Si la forma es grande, afectará el espaciado vertical del párrafo.
# No podemos mover esta forma a un lugar sin párrafo.
self.assertEqual(aw.drawing.WrapType.INLINE, shape.wrap_type)
self.assertTrue(shape.is_inline)
# 2 -  Flotante:
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, horz_pos=aw.drawing.RelativeHorizontalPosition.LEFT_MARGIN, left=200, vert_pos=aw.drawing.RelativeVerticalPosition.TOP_MARGIN, top=200, width=100, height=100, wrap_type=aw.drawing.WrapType.NONE)
shape.fill_color = aspose.pydrawing.Color.orange
# Una forma flotante pertenece al párrafo en el que la insertamos,
# lo cual podemos determinar mediante un símbolo de ancla que aparece al hacer clic en la forma.
# Si la forma no tiene un símbolo de ancla visible a su izquierda,
# necesitaremos habilitar anclas visibles mediante "Options" -> "Display" -> "Object Anchors".
# En Microsoft Word, podemos hacer clic izquierdo y arrastrar esta forma libremente a cualquier ubicación.
self.assertEqual(aw.drawing.WrapType.NONE, shape.wrap_type)
self.assertFalse(shape.is_inline)
doc.save(file_name=ARTIFACTS_DIR + 'Shape.IsInline.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

