---
title: DownsampleOptions.resolutionThreshold property
linktitle: resolutionThreshold property
articleTitle: resolutionThreshold property
second_title: Aspose.Words for Node.js
description: "DownsampleOptions.resolutionThreshold property. Specifies the threshold resolution in pixels per inch"
type: docs
weight: 40
url: /nodejs-net/aspose.words.saving/downsampleoptions/resolutionThreshold/
---

## DownsampleOptions.resolutionThreshold property

Specifies the threshold resolution in pixels per inch.
If resolution of an image in the document is less than threshold value,
the downsampling algorithm will not be applied.
A value of 0 means the threshold check is not used and all images that can be reduced in size are downsampled.


```js
get resolutionThreshold(): number
```

### Remarks

The default value is 0.


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
* class [DownsampleOptions](../)

