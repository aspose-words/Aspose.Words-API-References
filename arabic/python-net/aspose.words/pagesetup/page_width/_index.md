---
title: PageSetup.page_width property
linktitle: page_width property
articleTitle: page_width property
second_title: Aspose.Words for Python
description: "PageSetup.page_width property. Returns or sets the width of the page in points."
type: docs
weight: 340
url: /ar/python-net/aspose.words/pagesetup/page_width/
---

## PageSetup.page_width property

Returns or sets the width of the page in points.


```python
@property
def page_width(self) -> float:
    ...

@page_width.setter
def page_width(self, value: float):
    ...

```

### Examples

Shows how to insert an image, and use it as a watermark.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# أدرج الصورة في الترويسة بحيث تكون مرئية في كل صفحة.
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_PRIMARY)
shape = builder.insert_image(file_name=IMAGE_DIR + 'Transparent background logo.png')
shape.wrap_type = aw.drawing.WrapType.NONE
shape.behind_text = True
# ضع الصورة في مركز الصفحة.
shape.relative_horizontal_position = aw.drawing.RelativeHorizontalPosition.PAGE
shape.relative_vertical_position = aw.drawing.RelativeVerticalPosition.PAGE
shape.left = (builder.page_setup.page_width - shape.width) / 2
shape.top = (builder.page_setup.page_height - shape.height) / 2
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertWatermark.docx')
```

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
* class [PageSetup](../)

