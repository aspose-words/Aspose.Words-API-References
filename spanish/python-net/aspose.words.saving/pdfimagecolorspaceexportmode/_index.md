---
title: PdfImageColorSpaceExportMode enumeration
linktitle: PdfImageColorSpaceExportMode enumeration
articleTitle: PdfImageColorSpaceExportMode enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.PdfImageColorSpaceExportMode enumeration. Specifies how the color space will be selected for the images in PDF document."
type: docs
weight: 700
url: /es/python-net/aspose.words.saving/pdfimagecolorspaceexportmode/
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
# Cree un objeto "PdfSaveOptions" que podamos pasar al método "Save" del documento
# para modificar cómo ese método convierte el documento a .PDF.
pdf_save_options = aw.saving.PdfSaveOptions()
# Establezca la propiedad "ImageColorSpaceExportMode" a "PdfImageColorSpaceExportMode.Auto" para que Aspose.Words
# seleccione automáticamente el espacio de color para las imágenes en el documento que convierte a PDF.
# En la mayoría de los casos, el espacio de color será RGB.
# Establezca la propiedad "ImageColorSpaceExportMode" a "PdfImageColorSpaceExportMode.SimpleCmyk"
# para usar el espacio de color CMYK para todas las imágenes en el PDF guardado.
# Aspose.Words también aplicará compresión Flate a todas las imágenes e ignorará el valor de la propiedad "ImageCompression".
pdf_save_options.image_color_space_export_mode = pdf_image_color_space_export_mode
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.ImageColorSpaceExportMode.pdf', save_options=pdf_save_options)
```

### See Also

* module [aspose.words.saving](../)

