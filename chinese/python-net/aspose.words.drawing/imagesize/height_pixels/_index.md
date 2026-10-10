---
title: ImageSize.height_pixels property
linktitle: height_pixels property
articleTitle: height_pixels property
second_title: Aspose.Words for Python
description: "ImageSize.height_pixels property. Gets the height of the image in pixels."
type: docs
weight: 20
url: /zh/python-net/aspose.words.drawing/imagesize/height_pixels/
---

## ImageSize.height_pixels property

Gets the height of the image in pixels.


```python
@property
def height_pixels(self) -> int:
    ...

```

### Examples

Shows how to read the properties of an image in a shape.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 在文档中插入一个包含来自本地文件系统图像的形状。
shape = builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
# 如果形状包含图像，其 ImageData 属性将有效，
# 并且它将包含一个 ImageSize 对象。
image_size = shape.image_data.image_size
# ImageSize 对象包含关于形状内图像的只读信息。
self.assertEqual(400, image_size.height_pixels)
self.assertEqual(400, image_size.width_pixels)
delta = 0.05
self.assertAlmostEqual(95.98, image_size.horizontal_resolution, delta=delta)
self.assertAlmostEqual(95.98, image_size.vertical_resolution, delta=delta)
# 我们可以根据图像的尺寸来确定形状的大小，以避免拉伸图像。
shape.width = image_size.width_points * 2
shape.height = image_size.height_points * 2
doc.save(file_name=ARTIFACTS_DIR + 'Drawing.ImageSize.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ImageSize](../)

