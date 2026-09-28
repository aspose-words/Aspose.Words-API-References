---
title: PdfImageCompression enumeration
linktitle: PdfImageCompression enumeration
articleTitle: PdfImageCompression enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.PdfImageCompression enumeration. Specifies the type of compression applied to images in the PDF file."
type: docs
weight: 710
url: /zh/python-net/aspose.words.saving/pdfimagecompression/
---

## PdfImageCompression enumeration

Specifies the type of compression applied to images in the PDF file.


### Members

| Name | Description |
| --- | --- |
| AUTO | Automatically selects the most appropriate compression for each image. |
| JPEG | Jpeg compression. Does not support transparency. |

### Examples

Shows how to specify a compression type for all images in a document that we are converting to PDF.

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
# 将 "ImageCompression" 属性设置为 "PdfImageCompression.Auto" 以使用
# "ImageCompression" 属性用于控制最终输出 PDF 中 JPEG 图像的质量。
# 将 "ImageCompression" 属性设置为 "PdfImageCompression.Jpeg" 以使用
# "ImageCompression" 属性用于控制最终输出 PDF 中所有图像的质量。
pdf_save_options.image_compression = pdf_image_compression
# 将 "JpegQuality" 属性设置为 "10"，以在牺牲图像质量的代价下加强压缩。
pdf_save_options.jpeg_quality = 10
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.ImageCompression.pdf', save_options=pdf_save_options)
```

### See Also

* module [aspose.words.saving](../)

