---
title: PdfImageColorSpaceExportMode enumeration
linktitle: PdfImageColorSpaceExportMode enumeration
articleTitle: PdfImageColorSpaceExportMode enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.PdfImageColorSpaceExportMode enumeration. Specifies how the color space will be selected for the images in PDF document."
type: docs
weight: 700
url: /zh/python-net/aspose.words.saving/pdfimagecolorspaceexportmode/
---

## PdfImageColorSpaceExportMode enumeration

Specifies how the color space will be selected for the images in PDF document.


### Members

| Name | Description |
| --- | --- |
| AUTO | Aspose.Words automatically selects the most appropriate color space for each image. |
| SIMPLE_CMYK | Aspose.Words coverts RGB images to CMYK color space using simple formula. |

### Examples

Shows how to set a different color space for images in a document as we export it to PDF.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Jpeg image:')
builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
builder.insert_paragraph()
builder.writeln('Png image:')
builder.insert_image(file_name=IMAGE_DIR + 'Transparent background logo.png')
# 创建一个可以传递给文档的 \"Save\" 方法的 \"PdfSaveOptions\" 对象
# 以修改该方法将文档转换为 .PDF 的方式。
pdf_save_options = aw.saving.PdfSaveOptions()
# 将 "ImageColorSpaceExportMode" 属性设置为 "PdfImageColorSpaceExportMode.Auto" 以让 Aspose.Words
# 自动选择在转换为 PDF 时文档中图像的颜色空间。
# 在大多数情况下，颜色空间将是 RGB。
# 将 "ImageColorSpaceExportMode" 属性设置为 "PdfImageColorSpaceExportMode.SimpleCmyk"
# 以在保存的 PDF 中对所有图像使用 CMYK 颜色空间。
# Aspose.Words 还会对所有图像应用 Flate 压缩，并忽略 "ImageCompression" 属性的值。
pdf_save_options.image_color_space_export_mode = pdf_image_color_space_export_mode
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.ImageColorSpaceExportMode.pdf', save_options=pdf_save_options)
```

### See Also

* module [aspose.words.saving](../)

