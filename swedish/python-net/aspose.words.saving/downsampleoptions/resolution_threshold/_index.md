---
title: DownsampleOptions.resolution_threshold property
linktitle: resolution_threshold property
articleTitle: resolution_threshold property
second_title: Aspose.Words for Python
description: "DownsampleOptions.resolution_threshold property. Specifies the threshold resolution in pixels per inch"
type: docs
weight: 40
url: /sv/python-net/aspose.words.saving/downsampleoptions/resolution_threshold/
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
doc = aw.Document(file_name=MY_DIR + 'Images.docx')
# Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
# för att ändra hur den metoden konverterar dokumentet till .PDF.
options = aw.saving.PdfSaveOptions()
# Som standard minskar Aspose.Words alla bilder i ett dokument som vi sparar till PDF till 220 ppi.
self.assertTrue(options.downsample_options.downsample_images)
self.assertEqual(220, options.downsample_options.resolution)
self.assertEqual(0, options.downsample_options.resolution_threshold)
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.DownsampleOptions.Default.pdf', save_options=options)
# Ställ in egenskapen "Resolution" till "36" för att minska alla bilder till 36 ppi.
options.downsample_options.resolution = 36
# Ställ in egenskapen "ResolutionThreshold" för att endast tillämpa minskningen på
# bilder med en upplösning som är över 128 ppi.
options.downsample_options.resolution_threshold = 128
# Endast de två första bilderna från dokumentet kommer att minskas i detta steg.
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.DownsampleOptions.LowerResolution.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [DownsampleOptions](../)

