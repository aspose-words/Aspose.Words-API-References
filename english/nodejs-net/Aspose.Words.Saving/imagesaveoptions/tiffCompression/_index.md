---
title: ImageSaveOptions.tiffCompression property
linktitle: tiffCompression property
articleTitle: tiffCompression property
second_title: Aspose.Words for NodeJs
description: "ImageSaveOptions.tiffCompression property. Gets or sets the type of compression to apply when saving generated images to the TIFF format."
type: docs
weight: 150
url: /nodejs-net/Aspose.Words.Saving/imagesaveoptions/tiffCompression/
---

## ImageSaveOptions.tiffCompression property

Gets or sets the type of compression to apply when saving generated images to the TIFF format.


```js
get tiffCompression(): Aspose.Words.Saving.TiffCompression
```

### Remarks

Has effect only when saving to TIFF.

The default value is [TiffCompression.Lzw](../../tiffcompression/#Lzw).




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

* module [Aspose.Words.Saving](../../)
* class [ImageSaveOptions](../)

