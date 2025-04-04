---
title: DownsampleOptions class
linktitle: DownsampleOptions class
articleTitle: DownsampleOptions class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Saving.DownsampleOptions class. Allows to specify downsample options"
type: docs
weight: 140
url: /nodejs-net/aspose.words.saving/downsampleoptions/
---

## DownsampleOptions class

Allows to specify downsample options.
To learn more, visit the [Save a Document](https://docs.aspose.com/words/nodejs-net/save-a-document/) documentation article.




### Constructors
| Name | Description |
| --- | --- |
| [DownsampleOptions()](./constructor/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [downsampleImages](./downsampleImages/) | Specifies whether images should be downsampled. |
| [resolution](./resolution/) | Specifies the resolution in pixels per inch which the images should be downsampled to. |
| [resolutionThreshold](./resolutionThreshold/) | Specifies the threshold resolution in pixels per inch. If resolution of an image in the document is less than threshold value, the downsampling algorithm will not be applied. A value of 0 means the threshold check is not used and all images that can be reduced in size are downsampled. |

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

* module [Aspose.Words.Saving](../)

