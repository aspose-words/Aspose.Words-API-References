---
title: PdfImageColorSpaceExportMode enumeration
linktitle: PdfImageColorSpaceExportMode enumeration
articleTitle: PdfImageColorSpaceExportMode enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.PdfImageColorSpaceExportMode enumeration. Specifies how the color space will be selected for the images in PDF document."
type: docs
weight: 700
url: /de/python-net/aspose.words.saving/pdfimagecolorspaceexportmode/
---

## PdfImageColorSpaceExportMode enumeration

Specifies how the color space will be selected for the images in PDF document.


### Members

| Name | Description |
| --- | --- |
| AUTO | Aspose.Words automatically selects the most appropriate color space for each image. |
| SIMPLE_CMYK | Aspose.Words coverts RGB images to CMYK color space using simple formula. |

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
# Erstellen Sie ein "PdfSaveOptions"‑Objekt, das wir an die "Save"‑Methode des Dokuments übergeben können
# um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
pdf_save_options = aw.saving.PdfSaveOptions()
# Setzen Sie die "ImageColorSpaceExportMode"-Eigenschaft auf "PdfImageColorSpaceExportMode.Auto", um Aspose.Words zu
# automatisch den Farbraum für Bilder im Dokument auszuwählen, das es in PDF konvertiert.
# In den meisten Fällen wird der Farbraum RGB sein.
# Setzen Sie die Eigenschaft "ImageColorSpaceExportMode" auf "PdfImageColorSpaceExportMode.SimpleCmyk"
# um den CMYK-Farbraum für alle Bilder im gespeicherten PDF zu verwenden.
# Aspose.Words wendet ebenfalls Flate-Kompression auf alle Bilder an und ignoriert den Wert der Eigenschaft "ImageCompression".
pdf_save_options.image_color_space_export_mode = pdf_image_color_space_export_mode
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.ImageColorSpaceExportMode.pdf', save_options=pdf_save_options)
```

### See Also

* module [aspose.words.saving](../)

