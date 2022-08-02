---
title: tiff_compression property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets or sets the type of compression to apply when saving generated images to the TIFF format."
type: docs
weight: 150
url: /python-net/aspose.words.saving/imagesaveoptions/tiff_compression/
---

## ImageSaveOptions.tiff_compression property

Gets or sets the type of compression to apply when saving generated images to the TIFF format.

Has effect only when saving to TIFF.

The default value is [TiffCompression.LZW](../../tiffcompression/#LZW).




### Examples

Shows how to select the compression scheme to apply to a document that we convert into a TIFF image.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.insert_image(IMAGE_DIR + "Logo.jpg")

# Create an "ImageSaveOptions" object which we can pass to the document's "save" method
# to modify the way in which that method renders the document into an image.
options = aw.saving.ImageSaveOptions(aw.SaveFormat.TIFF)

# Set the "tiff_compression" property to "TiffCompression.NONE" to apply no compression while saving,
# which may result in a very large output file.
# Set the "tiff_compression" property to "TiffCompression.RLE" to apply RLE compression
# Set the "tiff_compression" property to "TiffCompression.LZW" to apply LZW compression.
# Set the "tiff_compression" property to "TiffCompression.CCITT3" to apply CCITT3 compression.
# Set the "tiff_compression" property to "TiffCompression.CCITT4" to apply CCITT4 compression.
options.tiff_compression = tiff_compression

doc.save(ARTIFACTS_DIR + "ImageSaveOptions.tiff_image_compression.tiff", options)

if tiff_compression == aw.saving.TiffCompression.NONE:
    self.assertLess(3000000, os.path.getsize(ARTIFACTS_DIR + "ImageSaveOptions.tiff_image_compression.tiff"))

elif tiff_compression == aw.saving.TiffCompression.RLE:
    self.assertLess(6000, os.path.getsize(ARTIFACTS_DIR + "ImageSaveOptions.tiff_image_compression.tiff"))

elif tiff_compression == aw.saving.TiffCompression.LZW:
    self.assertLess(200000, os.path.getsize(ARTIFACTS_DIR + "ImageSaveOptions.tiff_image_compression.tiff"))

elif tiff_compression == aw.saving.TiffCompression.CCITT3:
    self.assertGreater(90000, os.path.getsize(ARTIFACTS_DIR + "ImageSaveOptions.tiff_image_compression.tiff"))

elif tiff_compression == aw.saving.TiffCompression.CCITT4:
    self.assertGreater(20000, os.path.getsize(ARTIFACTS_DIR + "ImageSaveOptions.tiff_image_compression.tiff"))
```

### See Also

* module [aspose.words.saving](../../)
* class [ImageSaveOptions](../)

