---
title: interpolate_images property
second_title: Aspose.Words for Python via .NET API Reference
description: "A flag indicating whether image interpolation shall be performed by a conforming reader"
type: docs
weight: 180
url: /python-net/aspose.words.saving/pdfsaveoptions/interpolate_images/
---

## PdfSaveOptions.interpolate_images property

A flag indicating whether image interpolation shall be performed by a conforming reader.
When ``false`` is specified, the flag is not written to the output document and
the default behaviour of reader is used instead.


When the resolution of a source image is significantly lower than that of the output device,
each source sample covers many device pixels. As a result, images can appear jaggy or blocky.
These visual artifacts can be reduced by applying an image interpolation algorithm during rendering.
Instead of painting all pixels covered by a source sample with the same color, image interpolation
attempts to produce a smooth transition between adjacent sample values.

A conforming Reader may choose to not implement this feature of PDF,
or may use any specific implementation of interpolation that it wishes.

The default value is ``false``.

Interpolation flag is prohibited by PDF/A compliance. ``false`` value will be used automatically
when saving to PDF/A.




### Examples

Shows how to perform interpolation on images while saving a document to PDF.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

img = drawing.Image.from_file(IMAGE_DIR + "Transparent background logo.png")
builder.insert_image(img)

# Create a "PdfSaveOptions" object that we can pass to the document's "save" method
# to modify how that method converts the document to .PDF.
save_options = aw.saving.PdfSaveOptions()

# Set the "interpolate_images" property to "True" to get the reader that opens this document to interpolate images.
# Their resolution should be lower than that of the device that is displaying the document.
# Set the "interpolate_images" property to "False" to make it so that the reader does not apply any interpolation.
save_options.interpolate_images = interpolate_images

# When we open this document with a reader such as Adobe Acrobat, we will need to zoom in on the image
# to see the interpolation effect if we saved the document with it enabled.
doc.save(ARTIFACTS_DIR + "PdfSaveOptions.interpolate_images.pdf", save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

