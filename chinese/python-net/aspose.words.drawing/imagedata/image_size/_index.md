---
title: ImageData.image_size property
linktitle: image_size property
articleTitle: image_size property
second_title: Aspose.Words for Python
description: "ImageData.image_size property. Gets the information about image size and resolution."
type: docs
weight: 130
url: /zh/python-net/aspose.words.drawing/imagedata/image_size/
---

## ImageData.image_size property

Gets the information about image size and resolution.


```python
@property
def image_size(self) -> aspose.words.drawing.ImageSize:
    ...

```

### Remarks

If the image is linked only and not stored in the document, returns zero size.




### Examples

Shows how to resize a shape with an image.

```python
# 当我们使用 "InsertImage" 方法插入图像时，构建器会缩放显示图像的形状，使得，
# 在 Microsoft Word 中以 100% 缩放查看文档时，形状会以实际大小显示图像。
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
# 400×400 的图像将创建一个图像大小为 300×300pt 的 ImageData 对象。
image_size = shape.image_data.image_size
self.assertEqual(300, image_size.width_points)
self.assertEqual(300, image_size.height_points)
# 如果形状的尺寸与图像数据的尺寸匹配，
# 则形状以原始大小显示图像。
self.assertEqual(300, shape.width)
self.assertEqual(300, shape.height)
# 将形状的整体大小缩小 50%。
# 缩放因子同时作用于宽度和高度，以保持形状的比例。
shape.width *= 0.5
self.assertEqual(150, shape.width)
self.assertEqual(150, shape.height)
# 当您调整形状大小时，图像数据的尺寸保持不变。
self.assertEqual(300, image_size.width_points)
self.assertEqual(300, image_size.height_points)
# 我们可以参考图像数据的尺寸，根据图像大小应用缩放。
shape.width = image_size.width_points * 1.1
self.assertEqual(330, shape.width)
self.assertEqual(330, shape.height)
doc.save(file_name=ARTIFACTS_DIR + 'Image.ScaleImage.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ImageData](../)

