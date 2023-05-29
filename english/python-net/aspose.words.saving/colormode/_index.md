---
title: ColorMode enumeration
linktitle: ColorMode enumeration
articleTitle: ColorMode enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.ColorMode enumeration. Specifies how colors are rendered."
type: docs
weight: 20
url: /python-net/aspose.words.saving/colormode/
---

## ColorMode enumeration

Specifies how colors are rendered.


### Members

| Name | Description |
| --- | --- |
| NORMAL | Rendering with unmodified colors. |
| GRAYSCALE | Rendering with colors in a range of gray shades from white to black. |

### Examples

Shows how to change image color with saving options property.

```python
doc = aw.Document(MY_DIR + "Images.docx")

# Create a "PdfSaveOptions" object that we can pass to the document's "save" method
# to modify how that method converts the document to .PDF.
# Set the "color_mode" property to "GRAYSCALE" to render all images from the document in black and white.
# The size of the output document may be larger with this setting.
# Set the "color_mode" property to "NORMAL" to render all images in color.
pdf_save_options = aw.saving.PdfSaveOptions()
pdf_save_options.color_mode = color_mode

doc.save(ARTIFACTS_DIR + "PdfSaveOptions.color_rendering.pdf", pdf_save_options)
```

### See Also

* module [aspose.words.saving](../)

