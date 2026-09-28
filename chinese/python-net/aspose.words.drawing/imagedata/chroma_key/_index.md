---
title: ImageData.chroma_key property
linktitle: chroma_key property
articleTitle: chroma_key property
second_title: Aspose.Words for Python
description: "ImageData.chroma_key property. Defines the color value of the image that will be treated as transparent."
type: docs
weight: 40
url: /zh/python-net/aspose.words.drawing/imagedata/chroma_key/
---

## ImageData.chroma_key property

Defines the color value of the image that will be treated as transparent.


```python
@property
def chroma_key(self) -> aspose.pydrawing.Color:
    ...

@chroma_key.setter
def chroma_key(self, value: aspose.pydrawing.Color):
    ...

```

### Remarks

The default value is 0.




### Examples

Shows how to edit a shape's image data.

```python
img_source_doc = aw.Document(file_name=MY_DIR + 'Images.docx')
source_shape = img_source_doc.get_child_nodes(aw.NodeType.SHAPE, True)[0].as_shape()
dst_doc = aw.Document()
# 从源文档导入形状并将其追加到第一段。
imported_shape = dst_doc.import_node(src_node=source_shape, is_import_children=True).as_shape()
dst_doc.first_section.body.first_paragraph.append_child(imported_shape)
# 导入的形状包含图像。我们可以通过 ImageData 对象访问图像的属性和原始数据。
image_data = imported_shape.image_data
image_data.title = 'Imported Image'
self.assertTrue(image_data.has_image)
# 如果图像没有边框，其 ImageData 对象将把边框颜色定义为空。
self.assertEqual(4, image_data.borders.count)
self.assertEqual(aspose.pydrawing.Color.empty(), image_data.borders[0].color)
# 此图像未链接到本地文件系统中的其他形状或图像文件。
self.assertFalse(image_data.is_link)
self.assertFalse(image_data.is_link_only)
# “Brightness”和“Contrast”属性定义图像的亮度和对比度
# 在 0-1 的比例上，默认值为 0.5。
image_data.brightness = 0.8
image_data.contrast = 1
# 上述亮度和对比度值已生成一张大量白色的图像。
# 我们可以使用 ChromaKey 属性选择一种颜色并将其替换为透明，例如白色。
image_data.chroma_key = aspose.pydrawing.Color.white
# 再次导入源形状并将图像设置为单色。
imported_shape = dst_doc.import_node(src_node=source_shape, is_import_children=True).as_shape()
dst_doc.first_section.body.first_paragraph.append_child(imported_shape)
imported_shape.image_data.gray_scale = True
# 再次导入源形状以创建第三张图像并将其设置为 BiLevel。
# BiLevel 将每个像素设置为黑色或白色，以更接近原始颜色的为准。
imported_shape = dst_doc.import_node(src_node=source_shape, is_import_children=True).as_shape()
dst_doc.first_section.body.first_paragraph.append_child(imported_shape)
imported_shape.image_data.bi_level = True
# 裁剪在 0-1 的比例上确定。将一侧裁剪 0.3
# 将在裁剪的一侧裁掉图像的 30%。
imported_shape.image_data.crop_bottom = 0.3
imported_shape.image_data.crop_left = 0.3
imported_shape.image_data.crop_top = 0.3
imported_shape.image_data.crop_right = 0.3
dst_doc.save(file_name=ARTIFACTS_DIR + 'Drawing.ImageData.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ImageData](../)

