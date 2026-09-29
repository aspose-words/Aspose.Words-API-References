---
title: PdfImageCompression enumeration
linktitle: PdfImageCompression enumeration
articleTitle: PdfImageCompression enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.PdfImageCompression enumeration. Specifies the type of compression applied to images in the PDF file."
type: docs
weight: 710
url: /it/python-net/aspose.words.saving/pdfimagecompression/
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
# Crea un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
# per modificare il modo in cui quel metodo converte il documento in .PDF.
pdf_save_options = aw.saving.PdfSaveOptions()
# Imposta la proprietà "ImageCompression" a "PdfImageCompression.Auto" per utilizzare il
# proprietà "ImageCompression" per controllare la qualità delle immagini Jpeg che finiscono nel PDF di output.
# Imposta la proprietà "ImageCompression" a "PdfImageCompression.Jpeg" per utilizzare il
# proprietà "ImageCompression" per controllare la qualità di tutte le immagini che finiscono nel PDF di output.
pdf_save_options.image_compression = pdf_image_compression
# Imposta la proprietà "JpegQuality" a "10" per rafforzare la compressione a scapito della qualità dell'immagine.
pdf_save_options.jpeg_quality = 10
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.ImageCompression.pdf', save_options=pdf_save_options)
```

### See Also

* module [aspose.words.saving](../)

