---
title: TiffCompression enumeration
linktitle: TiffCompression enumeration
articleTitle: TiffCompression enumeration
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Saving.TiffCompression enumeration. Specifies what type of compression to apply when saving page images into a TIFF file."
type: docs
weight: 830
url: /nodejs-net/aspose.words.saving/tiffcompression/
---

## TiffCompression enumeration

Specifies what type of compression to apply when saving page images into a TIFF file.


### Members

| Name | Description |
| --- | --- |
| None | Specifies no compression. |
| Rle | Specifies the RLE compression scheme. |
| Lzw | Specifies the LZW compression scheme. In Java emulated by Deflate (Zip) compression. |
| Ccitt3 | Specifies the CCITT3 compression scheme. |
| Ccitt4 | Specifies the CCITT4 compression scheme. |

### Examples

Shows how to select the compression scheme to apply to a document that we convert into a TIFF image.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.insertImage(base.imageDir + "Logo.jpg");

// Create an "ImageSaveOptions" object which we can pass to the document's "Save" method
// to modify the way in which that method renders the document into an image.
let options = new aw.Saving.ImageSaveOptions(aw.SaveFormat.Tiff);
// Set the "TiffCompression" property to "TiffCompression.None" to apply no compression while saving,
// which may result in a very large output file.
// Set the "TiffCompression" property to "TiffCompression.Rle" to apply RLE compression
// Set the "TiffCompression" property to "TiffCompression.Lzw" to apply LZW compression.
// Set the "TiffCompression" property to "TiffCompression.Ccitt3" to apply CCITT3 compression.
// Set the "TiffCompression" property to "TiffCompression.Ccitt4" to apply CCITT4 compression.
options.tiffCompression = tiffCompression;

doc.save(base.artifactsDir + "ImageSaveOptions.TiffImageCompression.tiff", options);
```

### See Also

* module [Aspose.Words.Saving](../)

