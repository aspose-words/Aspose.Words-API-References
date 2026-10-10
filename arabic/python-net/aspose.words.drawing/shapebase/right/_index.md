---
title: ShapeBase.right property
linktitle: right property
articleTitle: right property
second_title: Aspose.Words for Python
description: "ShapeBase.right property. Gets the position of the right edge of the containing block of the shape."
type: docs
weight: 490
url: /ar/python-net/aspose.words.drawing/shapebase/right/
---

## ShapeBase.right property

Gets the position of the right edge of the containing block of the shape.


```python
@property
def right(self) -> float:
    ...

```

### Remarks

For a top-level shape, the value is in points and relative to the shape anchor.

For shapes in a group, the value is in the coordinate space and units of the parent group.




### Examples

Shows how to insert a floating image, and specify its position and size.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
shape.wrap_type = aw.drawing.WrapType.NONE
# قم بتكوين خاصية "RelativeHorizontalPosition" للshape لتعامل مع قيمة الخاصية "Left"
# كالمسافة الأفقية للشكل، بالنقاط، من الجانب الأيسر للصفحة.
shape.relative_horizontal_position = aw.drawing.RelativeHorizontalPosition.PAGE
# عيّن المسافة الأفقية للشكل من الجانب الأيسر للصفحة إلى 100.
shape.left = 100
# استخدم خاصية "RelativeVerticalPosition" بطريقة مماثلة لتحديد موضع الشكل 80 نقطة أسفل أعلى الصفحة.
shape.relative_vertical_position = aw.drawing.RelativeVerticalPosition.PAGE
shape.top = 80
# عيّن ارتفاع الشكل، والذي سيقوم تلقائيًا بتغيير عرض الشكل للحفاظ على الأبعاد.
shape.height = 125
self.assertEqual(125, shape.width)
# خاصيتي "Bottom" و "Right" تحتويان على الحافة السفلية واليمنى للصورة.
self.assertEqual(shape.top + shape.height, shape.bottom)
self.assertEqual(shape.left + shape.width, shape.right)
doc.save(file_name=ARTIFACTS_DIR + 'Image.CreateFloatingPositionSize.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

