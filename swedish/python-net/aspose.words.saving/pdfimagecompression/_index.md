---
title: PdfImageCompression enumeration
linktitle: PdfImageCompression enumeration
articleTitle: PdfImageCompression enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.PdfImageCompression enumeration. Specifies the type of compression applied to images in the PDF file."
type: docs
weight: 710
url: /sv/python-net/aspose.words.saving/pdfimagecompression/
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
# Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
# för att ändra hur den metoden konverterar dokumentet till .PDF.
pdf_save_options = aw.saving.PdfSaveOptions()
# Ställ in egenskapen "ImageCompression" till "PdfImageCompression.Auto" för att använda
# egenskapen "ImageCompression" för att kontrollera kvaliteten på JPEG-bilderna som hamnar i den färdiga PDF-filen.
# Ställ in egenskapen "ImageCompression" till "PdfImageCompression.Jpeg" för att använda
# egenskapen "ImageCompression" för att kontrollera kvaliteten på alla bilder som hamnar i den färdiga PDF-filen.
pdf_save_options.image_compression = pdf_image_compression
# Ställ in egenskapen "JpegQuality" till "10" för att stärka komprimeringen på bekostnad av bildkvaliteten.
pdf_save_options.jpeg_quality = 10
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.ImageCompression.pdf', save_options=pdf_save_options)
```

### See Also

* module [aspose.words.saving](../)

