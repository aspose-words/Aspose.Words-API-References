---
title: DownsampleOptions.resolution_threshold property
linktitle: resolution_threshold property
articleTitle: resolution_threshold property
second_title: Aspose.Words for Python
description: "DownsampleOptions.resolution_threshold property. Specifies the threshold resolution in pixels per inch"
type: docs
weight: 40
url: /python-net/aspose.words.saving/downsampleoptions/resolution_threshold/
---

## DownsampleOptions.resolution_threshold property

Specifies the threshold resolution in pixels per inch.
If resolution of an image in the document is less than threshold value,
the downsampling algorithm will not be applied.
A value of 0 means the threshold check is not used and all images that can be reduced in size are downsampled.


```python
@property
def resolution_threshold(self) -> int:
    ...

@resolution_threshold.setter
def resolution_threshold(self, value: int):
    ...

```

### Remarks

The default value is 0.


### Examples

Shows how to change the resolution of images in the PDF document.

```python
doc = aw.Document(MY_DIR + "Images.docx")

# Create a "PdfSaveOptions" object that we can pass to the document's "save" method
# to modify how that method converts the document to .PDF.
options = aw.saving.PdfSaveOptions()

# By default, Aspose.Words downsample all images in a document that we save to PDF to 220 ppi.
self.assertTrue(options.downsample_options.downsample_images)
self.assertEqual(220, options.downsample_options.resolution)
self.assertEqual(0, options.downsample_options.resolution_threshold)

doc.save(ARTIFACTS_DIR + "PdfSaveOptions.downsample_options.default.pdf", options)

# Set the "resolution" property to "36" to downsample all images to 36 ppi.
options.downsample_options.resolution = 36

# Set the "resolution_threshold" property to only apply the downsampling to
# images with a resolution that is above 128 ppi.
options.downsample_options.resolution_threshold = 128

# Only the first two images from the document will be downsampled at this stage.
doc.save(ARTIFACTS_DIR + "PdfSaveOptions.downsample_options.lower_resolution.pdf", options)
```

### See Also

* module [aspose.words.saving](../../)
* class [DownsampleOptions](../)

