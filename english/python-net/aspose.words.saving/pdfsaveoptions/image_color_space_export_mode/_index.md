---
title: PdfSaveOptions.image_color_space_export_mode property
linktitle: image_color_space_export_mode property
articleTitle: image_color_space_export_mode property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.image_color_space_export_mode property. Specifies how the color space will be selected for the images in PDF document."
type: docs
weight: 190
url: /python-net/aspose.words.saving/pdfsaveoptions/image_color_space_export_mode/
---

## PdfSaveOptions.image_color_space_export_mode property

Specifies how the color space will be selected for the images in PDF document.

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
builder = aw.DocumentBuilder(doc)

builder.writeln("Jpeg image:")
builder.insert_image(IMAGE_DIR + "Logo.jpg")
builder.insert_paragraph()
builder.writeln("Png image:")
builder.insert_image(IMAGE_DIR + "Transparent background logo.png")

# Create a "PdfSaveOptions" object that we can pass to the document's "save" method
# to modify how that method converts the document to .PDF.
pdf_save_options = aw.saving.PdfSaveOptions()

# Set the "image_color_space_export_mode" property to "PdfImageColorSpaceExportMode.AUTO" to get Aspose.Words to
# automatically select the color space for images in the document that it converts to PDF.
# In most cases, the color space will be RGB.
# Set the "image_color_space_export_mode" property to "PdfImageColorSpaceExportMode.SIMPLE_CMYK"
# to use the CMYK color space for all images in the saved PDF.
# Aspose.Words will also apply Flate compression to all images and ignore the "image_compression" property's value.
pdf_save_options.image_color_space_export_mode = pdf_image_color_space_export_mode

doc.save(ARTIFACTS_DIR + "PdfSaveOptions.image_color_space_export_mode.pdf", pdf_save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

