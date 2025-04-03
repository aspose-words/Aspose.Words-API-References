---
title: PdfSaveOptions.interpolateImages property
linktitle: interpolateImages property
articleTitle: interpolateImages property
second_title: Aspose.Words for NodeJs
description: "PdfSaveOptions.interpolateImages property. A flag indicating whether image interpolation shall be performed by a conforming reader"
type: docs
weight: 210
url: /nodejs-net/aspose.words.saving/pdfsaveoptions/interpolateImages/
---

## PdfSaveOptions.interpolateImages property

A flag indicating whether image interpolation shall be performed by a conforming reader.
When ``false`` is specified, the flag is not written to the output document and
the default behaviour of reader is used instead.



```js
get interpolateImages(): boolean
```

### Remarks

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

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.insertImage(base.imageDir + "Transparent background logo.png");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
let saveOptions = new aw.Saving.PdfSaveOptions();
// Set the "InterpolateImages" property to "true" to get the reader that opens this document to interpolate images.
// Their resolution should be lower than that of the device that is displaying the document.
// Set the "InterpolateImages" property to "false" to make it so that the reader does not apply any interpolation.
saveOptions.interpolateImages = interpolateImages;

// When we open this document with a reader such as Adobe Acrobat, we will need to zoom in on the image
// to see the interpolation effect if we saved the document with it enabled.
doc.save(base.artifactsDir + "PdfSaveOptions.interpolateImages.pdf", saveOptions);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [PdfSaveOptions](../)

