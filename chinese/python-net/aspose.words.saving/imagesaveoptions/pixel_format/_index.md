---
title: ImageSaveOptions.pixel_format property
linktitle: pixel_format property
articleTitle: pixel_format property
second_title: Aspose.Words for Python
description: "ImageSaveOptions.pixel_format property. Gets or sets the pixel format for the generated images."
type: docs
weight: 120
url: /zh/python-net/aspose.words.saving/imagesaveoptions/pixel_format/
---

## ImageSaveOptions.pixel_format property

Gets or sets the pixel format for the generated images.


```python
@property
def pixel_format(self) -> aspose.words.saving.ImagePixelFormat:
    ...

@pixel_format.setter
def pixel_format(self, value: aspose.words.saving.ImagePixelFormat):
    ...

```

### Remarks

This property has effect only when saving to raster image formats.

The default value is [ImagePixelFormat.FORMAT_32BPP_ARGB](../../imagepixelformat/#FORMAT_32BPP_ARGB).

Pixel format of the output image may differ from the set value
because of work of GDI+.




### Examples

Shows how to select a bit-per-pixel rate with which to render a document to an image.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.paragraph_format.style = doc.styles.get_by_name('Heading 1')
builder.writeln('Hello world!')
builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
# 当我们将文档保存为图像时，可以传递一个 SaveOptions 对象来
# 选择保存操作将生成的图像的像素格式。
# 不同的每像素位数会影响生成图像的质量和文件大小。
image_save_options = aw.saving.ImageSaveOptions(aw.SaveFormat.PNG)
image_save_options.pixel_format = image_pixel_format
# 我们可以克隆 ImageSaveOptions 实例。
self.assertNotEqual(image_save_options, image_save_options.clone())
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.PixelFormat.png', save_options=image_save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [ImageSaveOptions](../)

