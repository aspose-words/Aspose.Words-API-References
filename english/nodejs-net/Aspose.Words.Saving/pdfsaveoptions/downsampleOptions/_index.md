﻿---
title: PdfSaveOptions.downsampleOptions property
linktitle: downsampleOptions property
articleTitle: downsampleOptions property
second_title: Aspose.Words for Node.js
description: "PdfSaveOptions.downsampleOptions property. Allows to specify downsample options."
type: docs
weight: 110
url: /nodejs-net/aspose.words.saving/pdfsaveoptions/downsampleOptions/
---

## PdfSaveOptions.downsampleOptions property

Allows to specify downsample options.


```js
get downsampleOptions(): Aspose.Words.Saving.DownsampleOptions
```

### Examples

Shows how to change the resolution of images in the PDF document.

```js
let doc = new aw.Document(base.myDir + "Images.docx");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
let options = new aw.Saving.PdfSaveOptions();

// By default, Aspose.words downsample all images in a document that we save to PDF to 220 ppi.
expect(options.downsampleOptions.downsampleImages).toEqual(true);
expect(options.downsampleOptions.resolution).toEqual(220);
expect(options.downsampleOptions.resolutionThreshold).toEqual(0);

doc.save(base.artifactsDir + "PdfSaveOptions.downsampleOptions.default.pdf", options);

// Set the "Resolution" property to "36" to downsample all images to 36 ppi.
options.downsampleOptions.resolution = 36;

// Set the "ResolutionThreshold" property to only apply the downsampling to
// images with a resolution that is above 128 ppi.
options.downsampleOptions.resolutionThreshold = 128;

// Only the first two images from the document will be downsampled at this stage.
doc.save(base.artifactsDir + "PdfSaveOptions.downsampleOptions.LowerResolution.pdf", options);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [PdfSaveOptions](../)

