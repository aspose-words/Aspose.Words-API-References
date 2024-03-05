---
title: TiffCompression enumeration
linktitle: TiffCompression enumeration
articleTitle: TiffCompression enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.TiffCompression enumeration. Specifies what type of compression to apply when saving page images into a TIFF file."
type: docs
weight: 790
url: /python-net/aspose.words.saving/tiffcompression/
---

## TiffCompression enumeration

Specifies what type of compression to apply when saving page images into a TIFF file.


### Members

| Name | Description |
| --- | --- |
| NONE | Specifies no compression. |
| RLE | Specifies the RLE compression scheme. |
| LZW | Specifies the LZW compression scheme. In Java emulated by Deflate (Zip) compression. |
| CCITT3 | Specifies the CCITT3 compression scheme. |
| CCITT4 | Specifies the CCITT4 compression scheme. |

### Examples

Shows how to select the compression scheme to apply to a document that we convert into a TIFF image.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.insert_image(IMAGE_DIR + "Tagged Image File Format.tiff")

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

* module [aspose.words.saving](../)

