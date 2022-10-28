---
title: preblend_images property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets or sets a value determining whether or not to preblend transparent images with black background color."
type: docs
weight: 250
url: /python-net/aspose.words.saving/pdfsaveoptions/preblend_images/
---

## PdfSaveOptions.preblend_images property

Gets or sets a value determining whether or not to preblend transparent images with black background color.

Preblending images may improve PDF document visual appearance in Adobe Reader and remove anti-aliasing artifacts.

In order to properly display preblended images, PDF viewer application must support /Matte entry in soft-mask image dictionary.
Also preblending images may decrease PDF rendering performance.

The default value is ``False``.




### Examples

Shows how to preblend images with transparent backgrounds while saving a document to PDF.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

img = drawing.Image.from_file(IMAGE_DIR + "Transparent background logo.png")
builder.insert_image(img)

# Create a "PdfSaveOptions" object that we can pass to the document's "save" method
# to modify how that method converts the document to .PDF.
options = aw.saving.PdfSaveOptions()

# Set the "preblend_images" property to "True" to preblend transparent images
# with a background, which may reduce artifacts.
# Set the "preblend_images" property to "False" to render transparent images normally.
options.preblend_images = preblend_images

doc.save(ARTIFACTS_DIR + "PdfSaveOptions.preblend_images.pdf", options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

