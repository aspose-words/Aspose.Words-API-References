---
title: PdfSaveOptions.image_color_space_export_mode property
linktitle: image_color_space_export_mode property
articleTitle: image_color_space_export_mode property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.image_color_space_export_mode property. Specifies how the color space will be selected for the images in PDF document."
type: docs
weight: 210
url: /sv/python-net/aspose.words.saving/pdfsaveoptions/image_color_space_export_mode/
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
# Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
# för att ändra hur den metoden konverterar dokumentet till .PDF.
pdf_save_options = aw.saving.PdfSaveOptions()
# Ställ in egenskapen "ImageColorSpaceExportMode" till "PdfImageColorSpaceExportMode.Auto" för att få Aspose.Words att
# automatiskt välja färgrymden för bilder i dokumentet som det konverterar till PDF.
# In de flesta fall kommer färgrymden att vara RGB.
# Ställ in egenskapen "ImageColorSpaceExportMode" till "PdfImageColorSpaceExportMode.SimpleCmyk"
# för att använda CMYK-färgrymden för alla bilder i den sparade PDF-filen.
# Aspose.Words kommer också att tillämpa Flate-komprimering på alla bilder och ignorera värdet för egenskapen "ImageCompression".
pdf_save_options.image_color_space_export_mode = pdf_image_color_space_export_mode
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.ImageColorSpaceExportMode.pdf', save_options=pdf_save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

