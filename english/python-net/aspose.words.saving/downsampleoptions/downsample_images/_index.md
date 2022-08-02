---
title: downsample_images property
second_title: Aspose.Words for Python via .NET API Reference
description: "Specifies whether images should be downsampled."
type: docs
weight: 20
url: /python-net/aspose.words.saving/downsampleoptions/downsample_images/
---

## DownsampleOptions.downsample_images property

Specifies whether images should be downsampled.

The default value is ``true``.



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

