---
title: PdfSaveOptions.image_compression property
linktitle: image_compression property
articleTitle: image_compression property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.image_compression property. Specifies compression type to be used for all images in the document."
type: docs
weight: 220
url: /fr/python-net/aspose.words.saving/pdfsaveoptions/image_compression/
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

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

