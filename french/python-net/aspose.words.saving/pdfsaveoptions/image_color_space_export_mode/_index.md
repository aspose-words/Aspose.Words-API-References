---
title: PdfSaveOptions.image_color_space_export_mode property
linktitle: image_color_space_export_mode property
articleTitle: image_color_space_export_mode property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.image_color_space_export_mode property. Specifies how the color space will be selected for the images in PDF document."
type: docs
weight: 210
url: /fr/python-net/aspose.words.saving/pdfsaveoptions/image_color_space_export_mode/
---

## PdfSaveOptions.image_color_space_export_mode property

Specifies how the color space will be selected for the images in PDF document.


```python
@property
def image_color_space_export_mode(self) -> aspose.words.saving.PdfImageColorSpaceExportMode:
    ...

@image_color_space_export_mode.setter
def image_color_space_export_mode(self, value: aspose.words.saving.PdfImageColorSpaceExportMode):
    ...

```

### Remarks

The default value is [PdfImageColorSpaceExportMode.AUTO](../../pdfimagecolorspaceexportmode/#AUTO).


If [PdfImageColorSpaceExportMode.SIMPLE_CMYK](../../pdfimagecolorspaceexportmode/#SIMPLE_CMYK) value is specified,
[PdfSaveOptions.image_compression](../image_compression/) option is ignored and
Flate compression is used for all images in the document.


[PdfImageColorSpaceExportMode.SIMPLE_CMYK](../../pdfimagecolorspaceexportmode/#SIMPLE_CMYK) value is not supported when saving to PDF/A.
[PdfImageColorSpaceExportMode.AUTO](../../pdfimagecolorspaceexportmode/#AUTO) value will be used instead.




### Examples

Shows how to set a different color space for images in a document as we export it to PDF.

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
# Définissez la propriété "ImageColorSpaceExportMode" sur "PdfImageColorSpaceExportMode.Auto" pour que Aspose.Words
# sélectionne automatiquement l'espace colorimétrique des images du document qu'il convertit en PDF.
# Dans la plupart des cas, l'espace colorimétrique sera RGB.
# Définissez la propriété "ImageColorSpaceExportMode" sur "PdfImageColorSpaceExportMode.SimpleCmyk"
# pour utiliser l'espace colorimétrique CMYK pour toutes les images du PDF enregistré.
# Aspose.Words appliquera également la compression Flate à toutes les images et ignorera la valeur de la propriété "ImageCompression".
pdf_save_options.image_color_space_export_mode = pdf_image_color_space_export_mode
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.ImageColorSpaceExportMode.pdf', save_options=pdf_save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

