---
title: ShapeBase.is_inline property
linktitle: is_inline property
articleTitle: is_inline property
second_title: Aspose.Words for Python
description: "ShapeBase.is_inline property. A quick way to determine if this shape is positioned inline with text."
type: docs
weight: 310
url: /ar/python-net/aspose.words.drawing/shapebase/is_inline/
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
# فيما يلي نوعان من الالتفاف قد تكون للأشكال.
# 1 -  داخل السطر:
builder.write('Hello world! ')
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, width=100, height=100)
shape.fill_color = aspose.pydrawing.Color.light_blue
builder.write(' Hello again.')
# يُوجد الشكل داخل السطر داخل فقرة بين عناصر الفقرة الأخرى، مثل مقاطع النص.
# في Microsoft Word، يمكننا النقر وسحب الشكل إلى أي فقرة كما لو كان حرفًا.
# إذا كان الشكل كبيرًا، سيؤثر على تباعد الفقرات عموديًا.
# لا يمكننا نقل هذا الشكل إلى مكان لا يحتوي على فقرة.
self.assertEqual(aw.drawing.WrapType.INLINE, shape.wrap_type)
self.assertTrue(shape.is_inline)
# 2 -  عائم:
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, horz_pos=aw.drawing.RelativeHorizontalPosition.LEFT_MARGIN, left=200, vert_pos=aw.drawing.RelativeVerticalPosition.TOP_MARGIN, top=200, width=100, height=100, wrap_type=aw.drawing.WrapType.NONE)
shape.fill_color = aspose.pydrawing.Color.orange
# الشكل العائم ينتمي إلى الفقرة التي ندرجه فيها،
# ويمكننا تحديد ذلك برمز التثبيت الذي يظهر عندما ننقر على الشكل.
# إذا لم يكن لل shape رمز تثبيت مرئي على يساره،
# سنحتاج إلى تمكين الرموز المرئية عبر "Options" -> "Display" -> "Object Anchors".
# في Microsoft Word، يمكننا النقر بالزر الأيسر وسحب هذا الشكل بحرية إلى أي موقع.
self.assertEqual(aw.drawing.WrapType.NONE, shape.wrap_type)
self.assertFalse(shape.is_inline)
doc.save(file_name=ARTIFACTS_DIR + 'Shape.IsInline.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

