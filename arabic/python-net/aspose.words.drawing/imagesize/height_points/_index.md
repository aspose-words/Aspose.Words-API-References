---
title: ImageSize.height_points property
linktitle: height_points property
articleTitle: height_points property
second_title: Aspose.Words for Python
description: "ImageSize.height_points property. Gets the height of the image in points"
type: docs
weight: 30
url: /ar/python-net/aspose.words.drawing/imagesize/height_points/
---

## ImageSize.height_points property

Gets the height of the image in points. 1 point is 1/72 inch.


```python
@property
def height_points(self) -> float:
    ...

```

### Examples

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
* class [ImageSize](../)

