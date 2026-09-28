---
title: ImageSaveOptions.vertical_resolution property
linktitle: vertical_resolution property
articleTitle: vertical_resolution property
second_title: Aspose.Words for Python
description: "ImageSaveOptions.vertical_resolution property. Gets or sets the vertical resolution for the generated images, in dots per inch."
type: docs
weight: 190
url: /zh/python-net/aspose.words.saving/imagesaveoptions/vertical_resolution/
---

## ImageSaveOptions.vertical_resolution property

Gets or sets the vertical resolution for the generated images, in dots per inch.


```python
@property
def vertical_resolution(self) -> float:
    ...

@vertical_resolution.setter
def vertical_resolution(self, value: float):
    ...

```

### Remarks

This property has effect only when saving to raster image formats and affects the output size in pixels.

The default value is 96.




### Examples

Shows how to edit the image while Aspose.Words converts a document to one.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.paragraph_format.style = doc.styles.get_by_name('Heading 1')
builder.writeln('Hello world!')
builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
# 当我们将文档保存为图像时，可以传递一个 SaveOptions 对象来
# 在保存操作渲染图像时编辑该图像。
options = aw.saving.ImageSaveOptions(aw.SaveFormat.PNG)
# 我们可以调整这些属性来改变图像的亮度和对比度。
# 两者均采用 0-1 的比例，默认值为 0.5。
options.image_brightness = 0.3
options.image_contrast = 0.7
# 我们可以使用这些属性调整水平和垂直分辨率。
# 这将影响图像的尺寸。
# 这些属性的默认值为 96.0，对应分辨率为 96dpi。
options.horizontal_resolution = 72
options.vertical_resolution = 72
# 我们可以使用此属性缩放图像。默认值为 1.0，表示缩放 100%。
# 我们可以使用此属性抵消因更改分辨率而导致的图像尺寸变化。
options.scale = 96 / 72
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.EditImage.png', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [ImageSaveOptions](../)

