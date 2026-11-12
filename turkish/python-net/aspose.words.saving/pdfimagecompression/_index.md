---
title: PdfImageCompression enumeration
linktitle: PdfImageCompression enumeration
articleTitle: PdfImageCompression enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.PdfImageCompression enumeration. Specifies the type of compression applied to images in the PDF file."
type: docs
weight: 710
url: /tr/python-net/aspose.words.saving/pdfimagecompression/
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
# "PdfSaveOptions" nesnesi oluşturun; bu nesneyi belgenin "Save" metoduna geçebiliriz
# bu yöntemin belgeyi .PDF'ye nasıl dönüştürdüğünü değiştirmek için.
pdf_save_options = aw.saving.PdfSaveOptions()
# "ImageCompression" özelliğini "PdfImageCompression.Auto" olarak ayarlayın, kullanmak için
# "ImageCompression" özelliği, çıktı PDF'ye eklenen Jpeg görsellerin kalitesini kontrol eder.
# "ImageCompression" özelliğini "PdfImageCompression.Jpeg" olarak ayarlayın, kullanmak için
# "ImageCompression" özelliği, çıktı PDF'ye eklenen tüm görsellerin kalitesini kontrol eder.
pdf_save_options.image_compression = pdf_image_compression
# "JpegQuality" özelliğini "10" olarak ayarlayın, sıkıştırmayı artırmak için ancak görsel kalitesinden ödün verilir.
pdf_save_options.jpeg_quality = 10
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.ImageCompression.pdf', save_options=pdf_save_options)
```

### See Also

* module [aspose.words.saving](../)

