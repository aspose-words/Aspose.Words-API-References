---
title: ImageData.borders property
linktitle: borders property
articleTitle: borders property
second_title: Aspose.Words for Python
description: "ImageData.borders property. Gets the collection of borders of the image"
type: docs
weight: 20
url: /ar/python-net/aspose.words.drawing/imagedata/borders/
---

## ImageData.borders property

Gets the collection of borders of the image. Borders only have effect for inline images.


```python
@property
def borders(self) -> aspose.words.BorderCollection:
    ...

```

### Examples

Shows how to edit a shape's image data.

```python
img_source_doc = aw.Document(file_name=MY_DIR + 'Images.docx')
source_shape = img_source_doc.get_child_nodes(aw.NodeType.SHAPE, True)[0].as_shape()
dst_doc = aw.Document()
# استيراد شكل من المستند المصدر وإلحاقه بالفقرة الأولى.
imported_shape = dst_doc.import_node(src_node=source_shape, is_import_children=True).as_shape()
dst_doc.first_section.body.first_paragraph.append_child(imported_shape)
# الشكل المستورد يحتوي على صورة. يمكننا الوصول إلى خصائص الصورة والبيانات الخام عبر كائن ImageData.
image_data = imported_shape.image_data
image_data.title = 'Imported Image'
self.assertTrue(image_data.has_image)
# إذا كانت الصورة لا تحتوي على حدود، فسيحدد كائن ImageData لون الحدود كقيمة فارغة.
self.assertEqual(4, image_data.borders.count)
self.assertEqual(aspose.pydrawing.Color.empty(), image_data.borders[0].color)
# هذه الصورة لا ترتبط بشكل آخر أو ملف صورة في نظام الملفات المحلي.
self.assertFalse(image_data.is_link)
self.assertFalse(image_data.is_link_only)
# خصائص "Brightness" و "Contrast" تحدد سطوع الصورة وتباينها
# على مقياس من 0 إلى 1، مع القيمة الافتراضية عند 0.5.
image_data.brightness = 0.8
image_data.contrast = 1
# قيم السطوع والتباين المذكورة أعلاه أنشأت صورة تحتوي على الكثير من اللون الأبيض.
# يمكننا اختيار لون باستخدام خاصية ChromaKey لاستبداله بالشفافية، مثل الأبيض.
image_data.chroma_key = aspose.pydrawing.Color.white
# استورد الشكل المصدر مرة أخرى واضبط الصورة على أحادية اللون.
imported_shape = dst_doc.import_node(src_node=source_shape, is_import_children=True).as_shape()
dst_doc.first_section.body.first_paragraph.append_child(imported_shape)
imported_shape.image_data.gray_scale = True
# استورد الشكل المصدر مرة أخرى لإنشاء صورة ثالثة واضبطها على BiLevel.
# يقوم BiLevel بتعيين كل بكسل إما إلى الأسود أو الأبيض، أيهما أقرب إلى اللون الأصلي.
imported_shape = dst_doc.import_node(src_node=source_shape, is_import_children=True).as_shape()
dst_doc.first_section.body.first_paragraph.append_child(imported_shape)
imported_shape.image_data.bi_level = True
# يتم تحديد القص على مقياس من 0 إلى 1. قص جانب بنسبة 0.3
# سيتم قص 30٪ من الصورة على الجانب المقصوص.
imported_shape.image_data.crop_bottom = 0.3
imported_shape.image_data.crop_left = 0.3
imported_shape.image_data.crop_top = 0.3
imported_shape.image_data.crop_right = 0.3
dst_doc.save(file_name=ARTIFACTS_DIR + 'Drawing.ImageData.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ImageData](../)

