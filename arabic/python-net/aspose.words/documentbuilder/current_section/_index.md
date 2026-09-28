---
title: DocumentBuilder.current_section property
linktitle: current_section property
articleTitle: current_section property
second_title: Aspose.Words for Python
description: "DocumentBuilder.current_section property. Gets the section that is currently selected in this [DocumentBuilder](../)."
type: docs
weight: 60
url: /ar/python-net/aspose.words/documentbuilder/current_section/
---

## DocumentBuilder.current_section property

Gets the section that is currently selected in this [DocumentBuilder](../).



```python
@property
def current_section(self) -> aspose.words.Section:
    ...

```

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

* module [aspose.words](../../)
* class [DocumentBuilder](../)

