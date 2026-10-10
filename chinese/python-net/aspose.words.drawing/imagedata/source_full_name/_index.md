---
title: ImageData.source_full_name property
linktitle: source_full_name property
articleTitle: source_full_name property
second_title: Aspose.Words for Python
description: "ImageData.source_full_name property. Gets or sets the path and name of the source file for the linked image."
type: docs
weight: 170
url: /zh/python-net/aspose.words.drawing/imagedata/source_full_name/
---

## ImageData.source_full_name property

Gets or sets the path and name of the source file for the linked image.


```python
@property
def source_full_name(self) -> str:
    ...

@source_full_name.setter
def source_full_name(self, value: str):
    ...

```

### Remarks

The default value is an empty string.

If [ImageData.source_full_name](./) is not an empty string, the image is linked.




### Examples

Shows how to insert a linked image into a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
image_file_name = IMAGE_DIR + 'Windows MetaFile.wmf'
# 下面提供了两种将图像应用于形状以便显示的方法。
# 1 -  设置形状以包含图像。
shape = aw.drawing.Shape(builder.document, aw.drawing.ShapeType.IMAGE)
shape.wrap_type = aw.drawing.WrapType.INLINE
shape.image_data.set_image(file_name=image_file_name)
builder.insert_node(shape)
doc.save(file_name=ARTIFACTS_DIR + 'Image.CreateLinkedImage.Embedded.docx')
# 我们存储在形状中的每个图像都会增加文档的大小。
self.assertTrue(70000 < system_helper.io.FileInfo(ARTIFACTS_DIR + 'Image.CreateLinkedImage.Embedded.docx').length())
doc.first_section.body.first_paragraph.remove_all_children()
# 2 -  设置形状以链接到本地文件系统中的图像文件。
shape = aw.drawing.Shape(builder.document, aw.drawing.ShapeType.IMAGE)
shape.wrap_type = aw.drawing.WrapType.INLINE
shape.image_data.source_full_name = image_file_name
builder.insert_node(shape)
doc.save(file_name=ARTIFACTS_DIR + 'Image.CreateLinkedImage.Linked.docx')
# 链接图像可以节省空间，从而得到更小的文档。
# 然而，文档只能在
# 图像文件位于形状的 "SourceFullName" 属性指向的位置。
self.assertTrue(10000 > system_helper.io.FileInfo(ARTIFACTS_DIR + 'Image.CreateLinkedImage.Linked.docx').length())
```

### See Also

* module [aspose.words.drawing](../../)
* class [ImageData](../)

