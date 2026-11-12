---
title: ShapeBase.is_inline property
linktitle: is_inline property
articleTitle: is_inline property
second_title: Aspose.Words for Python
description: "ShapeBase.is_inline property. A quick way to determine if this shape is positioned inline with text."
type: docs
weight: 310
url: /tr/python-net/aspose.words.drawing/shapebase/is_inline/
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
# Aşağıda şekillerin sahip olabileceği iki sarma türü bulunmaktadır.
# 1 -  Satır içi:
builder.write('Hello world! ')
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, width=100, height=100)
shape.fill_color = aspose.pydrawing.Color.light_blue
builder.write(' Hello again.')
# Satır içi bir şekil, metin akışları gibi diğer paragraf öğeleri arasında bir paragraf içinde yer alır.
# Microsoft Word'de, şekli bir karaktermiş gibi herhangi bir paragraf içine tıklayıp sürükleyebiliriz.
# Şekil büyükse, dikey paragraf aralığını etkiler.
# Bu şekli paragrafı olmayan bir konuma taşıyamayız.
self.assertEqual(aw.drawing.WrapType.INLINE, shape.wrap_type)
self.assertTrue(shape.is_inline)
# 2 -  Yüzen:
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, horz_pos=aw.drawing.RelativeHorizontalPosition.LEFT_MARGIN, left=200, vert_pos=aw.drawing.RelativeVerticalPosition.TOP_MARGIN, top=200, width=100, height=100, wrap_type=aw.drawing.WrapType.NONE)
shape.fill_color = aspose.pydrawing.Color.orange
# Yüzen bir şekil, eklediğimiz paragrafın bir parçasıdır,
# bu, şekle tıkladığımızda görünen bir çapa simgesiyle belirlenebilir.
# Şeklin solunda görünür bir çapa simgesi yoksa,
# görünür çapaları "Options" -> "Display" -> "Object Anchors" üzerinden etkinleştirmemiz gerekir.
# Microsoft Word'de, bu şekle sol tıklayıp sürükleyerek istediğimiz yere özgürce taşıyabiliriz.
self.assertEqual(aw.drawing.WrapType.NONE, shape.wrap_type)
self.assertFalse(shape.is_inline)
doc.save(file_name=ARTIFACTS_DIR + 'Shape.IsInline.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

