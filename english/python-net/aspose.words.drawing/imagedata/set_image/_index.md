---
title: ImageData.set_image method
linktitle: set_image method
articleTitle: set_image method
second_title: Aspose.Words for Python
description: "aspose.words.drawing.ImageData.set_image method"
type: docs
weight: 210
url: /python-net/aspose.words.drawing/imagedata/set_image/
---

## set_image(stream) {#bytesio}

Sets the image that the shape displays.


```python
def set_image(self, stream: io.BytesIO):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | io.BytesIO | The stream that contains the image. |

## set_image(file_name) {#str}

Sets the image that the shape displays.


```python
def set_image(self, file_name: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| file_name | str | The image file. Can be a file name or a URL. |

## Examples

Shows how to display images from the local file system in a document.

```python
doc = aw.Document()
# To display an image in a document, we will need to create a shape
# which will contain an image, and then append it to the document's body.
img_shape = None
# Below are two ways of getting an image from a file in the local file system.
# 1 -  Create an image object from an image file:
with drawing.Image.from_file(IMAGE_DIR + 'Logo.jpg') as src_image:
    img_shape = aw.drawing.Shape(doc, aw.drawing.ShapeType.IMAGE)
    doc.first_section.body.first_paragraph.append_child(img_shape)
    img_shape.image_data.set_image(src_image)
# 2 -  Open an image file from the local file system using a stream:
with open(IMAGE_DIR + 'Logo.jpg', 'rb') as stream:
    img_shape = aw.drawing.Shape(doc, aw.drawing.ShapeType.IMAGE)
    doc.first_section.body.first_paragraph.append_child(img_shape)
    img_shape.image_data.set_image(stream)
    img_shape.left = 150.0
doc.save(ARTIFACTS_DIR + 'Drawing.import_image.docx')
```

Shows how to insert a linked image into a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
image_file_name = IMAGE_DIR + 'Windows MetaFile.wmf'
# Below are two ways of applying an image to a shape so that it can display it.
# 1 -  Set the shape to contain the image.
shape = aw.drawing.Shape(builder.document, aw.drawing.ShapeType.IMAGE)
shape.wrap_type = aw.drawing.WrapType.INLINE
shape.image_data.set_image(file_name=image_file_name)
builder.insert_node(shape)
doc.save(file_name=ARTIFACTS_DIR + 'Image.CreateLinkedImage.Embedded.docx')
# Every image that we store in shape will increase the size of our document.
self.assertTrue(70000 < system_helper.io.FileInfo(ARTIFACTS_DIR + 'Image.CreateLinkedImage.Embedded.docx').length())
doc.first_section.body.first_paragraph.remove_all_children()
# 2 -  Set the shape to link to an image file in the local file system.
shape = aw.drawing.Shape(builder.document, aw.drawing.ShapeType.IMAGE)
shape.wrap_type = aw.drawing.WrapType.INLINE
shape.image_data.source_full_name = image_file_name
builder.insert_node(shape)
doc.save(file_name=ARTIFACTS_DIR + 'Image.CreateLinkedImage.Linked.docx')
# Linking to images will save space and result in a smaller document.
# However, the document can only display the image correctly while
# the image file is present at the location that the shape's "SourceFullName" property points to.
self.assertTrue(10000 > system_helper.io.FileInfo(ARTIFACTS_DIR + 'Image.CreateLinkedImage.Linked.docx').length())
```

## See Also

* module [aspose.words.drawing](../../)
* class [ImageData](../)

