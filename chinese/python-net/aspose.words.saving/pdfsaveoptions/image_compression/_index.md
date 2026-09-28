---
title: PdfSaveOptions.image_compression property
linktitle: image_compression property
articleTitle: image_compression property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.image_compression property. Specifies compression type to be used for all images in the document."
type: docs
weight: 220
url: /zh/python-net/aspose.words.saving/pdfsaveoptions/image_compression/
---

## PdfSaveOptions.image_compression property

Specifies compression type to be used for all images in the document.


```python
@property
def image_compression(self) -> aspose.words.saving.PdfImageCompression:
    ...

@image_compression.setter
def image_compression(self, value: aspose.words.saving.PdfImageCompression):
    ...

```

### Remarks

Default is [PdfImageCompression.AUTO](../../pdfimagecompression/#AUTO).

Using [PdfImageCompression.JPEG](../../pdfimagecompression/#JPEG) lets you control the quality of images in the output document through the [PdfSaveOptions.jpeg_quality](../jpeg_quality/) property.

Using [PdfImageCompression.JPEG](../../pdfimagecompression/#JPEG) provides the fastest conversion speed when compared to the performance of other compression types,
but in this case, there is lossy JPEG compression.

Using [PdfImageCompression.AUTO](../../pdfimagecompression/#AUTO) lets to control the quality of Jpeg in the output document through the [PdfSaveOptions.jpeg_quality](../jpeg_quality/) property,
but for other formats, raw pixel data is extracted and saved with Flate compression.
This case is slower than Jpeg conversion but lossless.




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

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

