---
title: PdfImageCompression enumeration
linktitle: PdfImageCompression enumeration
articleTitle: PdfImageCompression enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.PdfImageCompression enumeration. Specifies the type of compression applied to images in the PDF file."
type: docs
weight: 710
url: /de/python-net/aspose.words.saving/pdfimagecompression/
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
# Erstellen Sie ein "PdfSaveOptions"‑Objekt, das wir an die "Save"‑Methode des Dokuments übergeben können
# um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
pdf_save_options = aw.saving.PdfSaveOptions()
# Setzen Sie die Eigenschaft "ImageCompression" auf "PdfImageCompression.Auto", um die
# "ImageCompression" property, um die Qualität der JPEG‑Bilder zu steuern, die im Ausgabepdf landen.
# Setzen Sie die Eigenschaft "ImageCompression" auf "PdfImageCompression.Jpeg", um die
# "ImageCompression" property, um die Qualität aller Bilder zu steuern, die im Ausgabepdf landen.
pdf_save_options.image_compression = pdf_image_compression
# Setzen Sie die Eigenschaft "JpegQuality" auf "10", um die Kompression zu verstärken, jedoch zulasten der Bildqualität.
pdf_save_options.jpeg_quality = 10
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.ImageCompression.pdf', save_options=pdf_save_options)
```

### See Also

* module [aspose.words.saving](../)

