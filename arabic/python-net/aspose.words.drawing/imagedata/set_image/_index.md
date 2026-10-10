---
title: ImageData.set_image method
linktitle: set_image method
articleTitle: set_image method
second_title: Aspose.Words for Python
description: "aspose.words.drawing.ImageData.set_image method"
type: docs
weight: 210
url: /ar/python-net/aspose.words.drawing/imagedata/set_image/
---

## set_image(stream) {#bytesio}

```python
def set_image(self, stream: io.BytesIO):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | io.BytesIO |  |

## set_image(file_name) {#str}

```python
def set_image(self, file_name: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| file_name | str |  |

## Examples

Shows how to insert a linked image into a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
image_file_name = IMAGE_DIR + 'Windows MetaFile.wmf'
# فيما يلي طريقتان لتطبيق صورة على شكل بحيث يمكنه عرضها.
# 1 -  اضبط الشكل ليحتوي على الصورة.
shape = aw.drawing.Shape(builder.document, aw.drawing.ShapeType.IMAGE)
shape.wrap_type = aw.drawing.WrapType.INLINE
shape.image_data.set_image(file_name=image_file_name)
builder.insert_node(shape)
doc.save(file_name=ARTIFACTS_DIR + 'Image.CreateLinkedImage.Embedded.docx')
# كل صورة نخزنها في الشكل ستزيد من حجم مستندنا.
self.assertTrue(70000 < system_helper.io.FileInfo(ARTIFACTS_DIR + 'Image.CreateLinkedImage.Embedded.docx').length())
doc.first_section.body.first_paragraph.remove_all_children()
# 2 -  اضبط الشكل ليرتبط بملف صورة في نظام الملفات المحلي.
shape = aw.drawing.Shape(builder.document, aw.drawing.ShapeType.IMAGE)
shape.wrap_type = aw.drawing.WrapType.INLINE
shape.image_data.source_full_name = image_file_name
builder.insert_node(shape)
doc.save(file_name=ARTIFACTS_DIR + 'Image.CreateLinkedImage.Linked.docx')
# ربط الصور سيوفر مساحة وينتج مستندًا أصغر.
# مع ذلك، لا يمكن للمستند عرض الصورة بشكل صحيح إلا أثناء
# ملف الصورة موجود في الموقع الذي تشير إليه خاصية "SourceFullName" للشكل.
self.assertTrue(10000 > system_helper.io.FileInfo(ARTIFACTS_DIR + 'Image.CreateLinkedImage.Linked.docx').length())
```

## See Also

* module [aspose.words.drawing](../../)
* class [ImageData](../)

