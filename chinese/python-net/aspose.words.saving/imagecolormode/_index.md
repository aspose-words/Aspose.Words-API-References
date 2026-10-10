---
title: ImageColorMode enumeration
linktitle: ImageColorMode enumeration
articleTitle: ImageColorMode enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.ImageColorMode enumeration. Specifies the color mode for the generated images of document pages."
type: docs
weight: 380
url: /zh/python-net/aspose.words.saving/imagecolormode/
---

## ImageColorMode enumeration

Specifies the color mode for the generated images of document pages.


### Members

| Name | Description |
| --- | --- |
| NONE | The pages of the document will be rendered as color images. |
| GRAYSCALE | The pages of the document will be rendered as grayscale images. |
| BLACK_AND_WHITE | The pages of the document will be rendered as black and white images. |

### Examples

Shows how to set a color mode when rendering documents.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.paragraph_format.style = doc.styles.get_by_name('Heading 1')
builder.writeln('Hello world!')
builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
# 当我们将文档保存为图像时，可以传递一个 SaveOptions 对象来
# 选择保存操作将生成的图像的颜色模式。
# 如果我们将 "ImageColorMode" 属性设置为 "ImageColorMode.BlackAndWhite"，
# 保存操作将在渲染文档时应用灰度颜色降低。
# 如果我们将 "ImageColorMode" 属性设置为 "ImageColorMode.Grayscale"，
# 保存操作将把文档渲染为单色图像。
# 如果我们将 "ImageColorMode" 属性设置为 "None"，保存操作将使用默认方法
# 并在输出图像中保留文档的所有颜色。
image_save_options = aw.saving.ImageSaveOptions(aw.SaveFormat.PNG)
image_save_options.image_color_mode = image_color_mode
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.ColorMode.png', save_options=image_save_options)
```

### See Also

* module [aspose.words.saving](../)

