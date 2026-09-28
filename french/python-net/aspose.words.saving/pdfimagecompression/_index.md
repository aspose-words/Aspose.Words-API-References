---
title: PdfImageCompression enumeration
linktitle: PdfImageCompression enumeration
articleTitle: PdfImageCompression enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.PdfImageCompression enumeration. Specifies the type of compression applied to images in the PDF file."
type: docs
weight: 710
url: /fr/python-net/aspose.words.saving/pdfimagecompression/
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
# Créez un objet "PdfSaveOptions" que nous pouvons transmettre à la méthode "Save" du document
# pour modifier la façon dont cette méthode convertit le document en .PDF.
pdf_save_options = aw.saving.PdfSaveOptions()
# Définissez la propriété "ImageCompression" à "PdfImageCompression.Auto" pour utiliser le
# la propriété "ImageCompression" pour contrôler la qualité des images Jpeg qui se retrouvent dans le PDF de sortie.
# Définissez la propriété "ImageCompression" à "PdfImageCompression.Jpeg" pour utiliser le
# la propriété "ImageCompression" pour contrôler la qualité de toutes les images qui se retrouvent dans le PDF de sortie.
pdf_save_options.image_compression = pdf_image_compression
# Définissez la propriété "JpegQuality" à "10" pour renforcer la compression au détriment de la qualité de l'image.
pdf_save_options.jpeg_quality = 10
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.ImageCompression.pdf', save_options=pdf_save_options)
```

### See Also

* module [aspose.words.saving](../)

