---
title: FixedPageSaveOptions.color_mode property
linktitle: color_mode property
articleTitle: color_mode property
second_title: Aspose.Words for Python
description: "FixedPageSaveOptions.color_mode property. Gets or sets a value determining how colors are rendered."
type: docs
weight: 10
url: /zh/python-net/aspose.words.saving/fixedpagesaveoptions/color_mode/
---

## FixedPageSaveOptions.color_mode property

Gets or sets a value determining how colors are rendered.


```python
@property
def color_mode(self) -> aspose.words.saving.ColorMode:
    ...

@color_mode.setter
def color_mode(self, value: aspose.words.saving.ColorMode):
    ...

```

### Remarks

The default value is [ColorMode.NORMAL](../../colormode/#NORMAL).



### Examples

Shows how to change image color with saving options property.

```python
doc = aw.Document(file_name=MY_DIR + 'Images.docx')
# 创建一个可以传递给文档的 \"Save\" 方法的 \"PdfSaveOptions\" 对象
# 以修改该方法将文档转换为 .PDF 的方式。
# 将 "ColorMode" 属性设置为 "Grayscale"，以将文档中的所有图像渲染为黑白。
# 使用此设置时，输出文档的大小可能会变大。
# 将 "ColorMode" 属性设置为 "Normal"，以将所有图像渲染为彩色。
pdf_save_options = aw.saving.PdfSaveOptions()
pdf_save_options.color_mode = color_mode
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.ColorRendering.pdf', save_options=pdf_save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [FixedPageSaveOptions](../)

