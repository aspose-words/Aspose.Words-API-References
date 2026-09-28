---
title: HtmlSaveOptions.scale_image_to_shape_size property
linktitle: scale_image_to_shape_size property
articleTitle: scale_image_to_shape_size property
second_title: Aspose.Words for Python
description: "HtmlSaveOptions.scale_image_to_shape_size property. Specifies whether images are scaled by Aspose.Words to the bounding shape size when exporting to HTML, MHTML or EPUB"
type: docs
weight: 470
url: /zh/python-net/aspose.words.saving/htmlsaveoptions/scale_image_to_shape_size/
---

## HtmlSaveOptions.scale_image_to_shape_size property

Specifies whether images are scaled by Aspose.Words to the bounding shape size when exporting to HTML, MHTML
or EPUB.
Default value is ``True``.



```python
@property
def scale_image_to_shape_size(self) -> bool:
    ...

@scale_image_to_shape_size.setter
def scale_image_to_shape_size(self, value: bool):
    ...

```

### Remarks

An image in a Microsoft Word document is a shape. The shape has a size and the image
has its own size. The sizes are not directly linked. For example, the image can be 1024x786 pixels,
but shape that displays this image can be 400x300 points.

In order to display an image in the browser, it must be scaled to the shape size.
The [HtmlSaveOptions.scale_image_to_shape_size](./) property controls where the scaling of the image
takes place: in Aspose.Words during export to HTML or in the browser when displaying the document.

When [HtmlSaveOptions.scale_image_to_shape_size](./) is ``True``, the image is scaled by Aspose.Words
using high quality scaling during export to HTML. When [HtmlSaveOptions.scale_image_to_shape_size](./)
is ``False``, the image is output with its original size and the browser has to scale it.

In general, browsers do quick and poor quality scaling. As a result, you will normally get better
display quality in the browser and smaller file size when [HtmlSaveOptions.scale_image_to_shape_size](./) is ``True``,
but better printing quality and faster conversion when [HtmlSaveOptions.scale_image_to_shape_size](./) is ``False``.

In addition to shapes containing individual raster images, this option also affects group shapes consisting
of raster images. If [HtmlSaveOptions.scale_image_to_shape_size](./) is ``False`` and a group shape contains raster images
whose intrinsic resolution is higher than the value specified in [HtmlSaveOptions.image_resolution](../image_resolution/), Aspose.Words will
increase rendering resolution for that group. This allows to better preserve quality of grouped high resolution
images when saving to HTML.




### Examples

Shows how to disable the scaling of images to their parent shape dimensions when saving to .html.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 插入一个包含图像的形状，然后使该形状明显小于图像。
image_shape = builder.insert_image(file_name=IMAGE_DIR + 'Transparent background logo.png')
image_shape.width = 50
image_shape.height = 50
# 将包含带图像形状的文档保存为 HTML 会在本地文件系统中创建图像文件
# 对于每个此类形状。输出的 HTML 文档将使用 <image> 标签来链接和显示这些图像。
# 当我们将文档保存为 HTML 时，可以传递一个 SaveOptions 对象来确定
# 是否将形状内部的所有图像缩放到其形状的大小。
# 将 "ScaleImageToShapeSize" 标志设置为 "true" 将缩小每个图像
# 到包含它的形状的大小，从而没有保存的图像会大于文档所需的大小。
# 将 "ScaleImageToShapeSize" 标志设置为 "false" 将保留这些图像的原始大小，
# 这将占用更多空间，以换取图像质量的保留。
options = aw.saving.HtmlSaveOptions()
options.scale_image_to_shape_size = scale_image_to_shape_size
doc.save(file_name=ARTIFACTS_DIR + 'HtmlSaveOptions.ScaleImageToShapeSize.html', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlSaveOptions](../)
* property [HtmlSaveOptions.image_resolution](../image_resolution/)

