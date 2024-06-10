---
title: FixedPageSaveOptions.color_mode property
linktitle: color_mode property
articleTitle: color_mode property
second_title: Aspose.Words for Python
description: "FixedPageSaveOptions.color_mode property. Gets or sets a value determining how colors are rendered."
type: docs
weight: 10
url: /python-net/aspose.words.saving/fixedpagesaveoptions/color_mode/
---

## FixedPageSaveOptions.color_mode property

Gets or sets a value determining how colors are rendered.


```python
@property
def color_mode(self) -> aspose.words.saving.ColorMode:
    ...

@color_mode.setter
def color_mode(self, value: aspose.words.saving.ColorMode):
    ...

```

### Remarks

The default value is [ColorMode.NORMAL](../../colormode/#NORMAL).



### Examples

Shows how to change image color with saving options property.

```python
doc = aw.Document(MY_DIR + 'Images.docx')
# Create a "PdfSaveOptions" object that we can pass to the document's "save" method
# to modify how that method converts the document to .PDF.
# Set the "color_mode" property to "GRAYSCALE" to render all images from the document in black and white.
# The size of the output document may be larger with this setting.
# Set the "color_mode" property to "NORMAL" to render all images in color.
pdf_save_options = aw.saving.PdfSaveOptions()
pdf_save_options.color_mode = color_mode
doc.save(ARTIFACTS_DIR + 'PdfSaveOptions.color_rendering.pdf', pdf_save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [FixedPageSaveOptions](../)

