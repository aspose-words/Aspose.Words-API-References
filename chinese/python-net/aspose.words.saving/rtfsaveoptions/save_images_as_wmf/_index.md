---
title: RtfSaveOptions.save_images_as_wmf property
linktitle: save_images_as_wmf property
articleTitle: save_images_as_wmf property
second_title: Aspose.Words for Python
description: "RtfSaveOptions.save_images_as_wmf property. When ``True`` all images will be saved as WMF."
type: docs
weight: 50
url: /zh/python-net/aspose.words.saving/rtfsaveoptions/save_images_as_wmf/
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
# 创建一个 "RtfSaveOptions" 对象，以传递给文档的 "Save" 方法，修改我们将其保存为 RTF 的方式。
rtf_save_options = aw.saving.RtfSaveOptions()
# 将 "SaveImagesAsWmf" 属性设置为 "true"，在保存为 RTF 时将文档中的所有图像转换为 WMF。
# 这样做将帮助诸如 WordPad 等阅读器读取我们的文档。
# 将 "SaveImagesAsWmf" 属性设置为 "false"，以保留文档中所有图像的原始格式
# 在我们将其保存为 RTF 时。这将以兼容旧版 RTF 阅读器为代价，保留图像质量。
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

