---
title: PdfImageCompression enumeration
linktitle: PdfImageCompression enumeration
articleTitle: PdfImageCompression enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.PdfImageCompression enumeration. Specifies the type of compression applied to images in the PDF file."
type: docs
weight: 710
url: /ar/python-net/aspose.words.saving/pdfimagecompression/
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
# أنشئ كائن "PdfSaveOptions" يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
# لتعديل طريقة تحويل تلك الطريقة للمستند إلى .PDF.
pdf_save_options = aw.saving.PdfSaveOptions()
# قم بتعيين الخاصية "ImageCompression" إلى "PdfImageCompression.Auto" لاستخدام الـ
# خاصية "ImageCompression" للتحكم في جودة صور Jpeg التي تنتهي في ملف PDF الناتج.
# قم بتعيين الخاصية "ImageCompression" إلى "PdfImageCompression.Jpeg" لاستخدام الـ
# خاصية "ImageCompression" للتحكم في جودة جميع الصور التي تنتهي في ملف PDF الناتج.
pdf_save_options.image_compression = pdf_image_compression
# قم بتعيين الخاصية "JpegQuality" إلى "10" لتعزيز الضغط على حساب جودة الصورة.
pdf_save_options.jpeg_quality = 10
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.ImageCompression.pdf', save_options=pdf_save_options)
```

### See Also

* module [aspose.words.saving](../)

