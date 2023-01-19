---
title: PdfImageColorSpaceExportMode enumeration
second_title: Aspose.Words for Python via .NET API Reference
description: "Specifies how the color space will be selected for the images in PDF document."
type: docs
weight: 620
url: /python-net/aspose.words.saving/pdfimagecolorspaceexportmode/
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

* module [aspose.words.saving](../)

