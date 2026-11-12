---
title: PdfImageCompression enumeration
linktitle: PdfImageCompression enumeration
articleTitle: PdfImageCompression enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.PdfImageCompression enumeration. Specifies the type of compression applied to images in the PDF file."
type: docs
weight: 710
url: /ru/python-net/aspose.words.saving/pdfimagecompression/
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
# Создайте объект "PdfSaveOptions", который мы можем передать методу "Save" документа
# чтобы изменить способ, которым этот метод конвертирует документ в .PDF.
pdf_save_options = aw.saving.PdfSaveOptions()
# Установите свойство "ImageCompression" в значение "PdfImageCompression.Auto", чтобы использовать
# свойство "ImageCompression" для контроля качества JPEG‑изображений, попадающих в выходной PDF.
# Установите свойство "ImageCompression" в значение "PdfImageCompression.Jpeg", чтобы использовать
# свойство "ImageCompression" для контроля качества всех изображений, попадающих в выходной PDF.
pdf_save_options.image_compression = pdf_image_compression
# Установите свойство "JpegQuality" в значение "10", чтобы усилить сжатие за счёт качества изображения.
pdf_save_options.jpeg_quality = 10
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.ImageCompression.pdf', save_options=pdf_save_options)
```

### See Also

* module [aspose.words.saving](../)

