---
title: ImageSaveOptions.scale property
linktitle: scale property
articleTitle: scale property
second_title: Aspose.Words for Python
description: "ImageSaveOptions.scale property. Gets or sets the zoom factor for the generated images."
type: docs
weight: 140
url: /zh/python-net/aspose.words.saving/imagesaveoptions/scale/
---

## ImageSaveOptions.scale property

Gets or sets the zoom factor for the generated images.


```python
@property
def scale(self) -> float:
    ...

@scale.setter
def scale(self, value: float):
    ...

```

### Remarks

The default value is 1.0. The value must be greater than 0.


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

Shows how to render an Office Math object into an image file in the local file system.

```python
from api_example_base import ApiExampleBase, MY_DIR, ARTIFACTS_DIR, GOLDS_DIR, TEMP_DIR, IMAGE_DIR, FONTS_DIR
import aspose.words as aw
doc = aw.Document(file_name=MY_DIR + 'Office math.docx')
math = doc.get_child(aw.NodeType.OFFICE_MATH, 0, True).as_office_math()
# 创建一个 "ImageSaveOptions" 对象，以传递给节点渲染器的 "Save" 方法进行修改
# 它如何将 OfficeMath 节点渲染为图像。
save_options = aw.saving.ImageSaveOptions(aw.SaveFormat.PNG)
# 将 "Scale" 属性设置为 5，以将对象渲染为原始大小的五倍。
save_options.scale = 5
math.get_math_renderer().save(file_name=ARTIFACTS_DIR + 'Shape.RenderOfficeMath.png', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [ImageSaveOptions](../)

