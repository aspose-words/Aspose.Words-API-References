---
title: RtfSaveOptions.save_images_as_wmf property
linktitle: save_images_as_wmf property
articleTitle: save_images_as_wmf property
second_title: Aspose.Words for Python
description: "RtfSaveOptions.save_images_as_wmf property. When ``True`` all images will be saved as WMF."
type: docs
weight: 50
url: /ar/python-net/aspose.words.saving/rtfsaveoptions/save_images_as_wmf/
---

## RtfSaveOptions.save_images_as_wmf property

When ``True`` all images will be saved as WMF.



```python
@property
def save_images_as_wmf(self) -> bool:
    ...

@save_images_as_wmf.setter
def save_images_as_wmf(self, value: bool):
    ...

```

### Remarks

This option might help to avoid WordPad warning messages.


### Examples

Shows how to convert all images in a document to the Windows Metafile format as we save the document as an RTF.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Jpeg image:')
image_shape = builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
self.assertEqual(aw.drawing.ImageType.JPEG, image_shape.image_data.image_type)
builder.insert_paragraph()
builder.writeln('Png image:')
image_shape = builder.insert_image(file_name=IMAGE_DIR + 'Transparent background logo.png')
self.assertEqual(aw.drawing.ImageType.PNG, image_shape.image_data.image_type)
# أنشئ كائن "RtfSaveOptions" لتمريره إلى طريقة "Save" الخاصة بالمستند لتعديل طريقة حفظه كملف RTF.
rtf_save_options = aw.saving.RtfSaveOptions()
# عيّن خاصية \"SaveImagesAsWmf\" إلى \"true\" لتحويل جميع الصور في المستند إلى WMF عند حفظه كـ RTF.
# سيساعد ذلك القارئات مثل WordPad على قراءة مستندنا.
# عيّن خاصية \"SaveImagesAsWmf\" إلى \"false\" للحفاظ على الصيغة الأصلية لجميع الصور في المستند
# عند حفظه كـ RTF. سيحافظ ذلك على جودة الصور على حساب التوافق مع قارئات RTF القديمة.
rtf_save_options.save_images_as_wmf = save_images_as_wmf
doc.save(file_name=ARTIFACTS_DIR + 'RtfSaveOptions.SaveImagesAsWmf.rtf', save_options=rtf_save_options)
doc = aw.Document(file_name=ARTIFACTS_DIR + 'RtfSaveOptions.SaveImagesAsWmf.rtf')
shapes = doc.get_child_nodes(aw.NodeType.SHAPE, True)
if save_images_as_wmf:
    self.assertEqual(aw.drawing.ImageType.WMF, shapes[0].as_shape().image_data.image_type)
    self.assertEqual(aw.drawing.ImageType.WMF, shapes[1].as_shape().image_data.image_type)
else:
    self.assertEqual(aw.drawing.ImageType.JPEG, shapes[0].as_shape().image_data.image_type)
    self.assertEqual(aw.drawing.ImageType.PNG, shapes[1].as_shape().image_data.image_type)
```

### See Also

* module [aspose.words.saving](../../)
* class [RtfSaveOptions](../)

