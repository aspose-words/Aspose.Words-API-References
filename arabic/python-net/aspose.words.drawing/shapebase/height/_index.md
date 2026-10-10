---
title: ShapeBase.height property
linktitle: height property
articleTitle: height property
second_title: Aspose.Words for Python
description: "ShapeBase.height property. Gets or sets the height of the containing block of the shape."
type: docs
weight: 210
url: /ar/python-net/aspose.words.drawing/shapebase/height/
---

## ShapeBase.height property

Gets or sets the height of the containing block of the shape.


```python
@property
def height(self) -> float:
    ...

@height.setter
def height(self, value: float):
    ...

```

### Remarks

For a top-level shape, the value is in points.

For shapes in a group, the value is in the coordinate space and units of the parent group.

The default value is 0.




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

Shows how to resize a shape with an image.

```python
# عند إدراج صورة باستخدام طريقة "InsertImage"، يقوم المُنشئ بتحجيم الشكل الذي يعرض الصورة بحيث،
# عند عرض المستند بنسبة تكبير 100٪ في Microsoft Word، يعرض الشكل الصورة بحجمها الفعلي.
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
# صورة بحجم 400×400 ستُنشئ كائن ImageData بحجم صورة 300×300 نقطة.
image_size = shape.image_data.image_size
self.assertEqual(300, image_size.width_points)
self.assertEqual(300, image_size.height_points)
# إذا كانت أبعاد الشكل مطابقة لأبعاد بيانات الصورة،
# فإن الشكل يعرض الصورة بحجمها الأصلي.
self.assertEqual(300, shape.width)
self.assertEqual(300, shape.height)
# قلل الحجم الكلي للشكل بنسبة 50٪.
# عوامل التحجيم تُطبق على العرض والارتفاع معًا للحفاظ على نسب الشكل.
shape.width *= 0.5
self.assertEqual(150, shape.width)
self.assertEqual(150, shape.height)
# عند تغيير حجم الشكل، يبقى حجم بيانات الصورة كما هو.
self.assertEqual(300, image_size.width_points)
self.assertEqual(300, image_size.height_points)
# يمكننا الرجوع إلى أبعاد بيانات الصورة لتطبيق تحجيم بناءً على حجم الصورة.
shape.width = image_size.width_points * 1.1
self.assertEqual(330, shape.width)
self.assertEqual(330, shape.height)
doc.save(file_name=ARTIFACTS_DIR + 'Image.ScaleImage.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

