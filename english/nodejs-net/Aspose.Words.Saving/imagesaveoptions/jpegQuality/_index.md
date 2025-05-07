---
title: ImageSaveOptions.jpegQuality property
linktitle: jpegQuality property
articleTitle: jpegQuality property
second_title: Aspose.Words for Node.js
description: "ImageSaveOptions.jpegQuality property. Gets or sets a value determining the quality of the generated JPEG images."
type: docs
weight: 60
url: /nodejs-net/aspose.words.saving/imagesaveoptions/jpegQuality/
---

## ImageSaveOptions.jpegQuality property

Gets or sets a value determining the quality of the generated JPEG images.


```js
get jpegQuality(): number
```

### Remarks

Has effect only when saving to JPEG.

Use this property to get or set the quality of generated images when saving in JPEG format.
The value may vary from 0 to 100 where 0 means worst quality but maximum compression and 100
means best quality but minimum compression.

The default value is 95.




### Examples

Shows how to configure compression while saving a document as a JPEG.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);
builder.insertImage(base.imageDir + "Logo.jpg");

// Create an "ImageSaveOptions" object which we can pass to the document's "Save" method
// to modify the way in which that method renders the document into an image.
let imageOptions = new aw.Saving.ImageSaveOptions(aw.SaveFormat.Jpeg);
// Set the "JpegQuality" property to "10" to use stronger compression when rendering the document.
// This will reduce the file size of the document, but the image will display more prominent compression artifacts.
imageOptions.jpegQuality = 10;
doc.save(base.artifactsDir + "ImageSaveOptions.jpegQuality.HighCompression.jpg", imageOptions);

// Set the "JpegQuality" property to "100" to use weaker compression when rending the document.
// This will improve the quality of the image at the cost of an increased file size.
imageOptions.jpegQuality = 100;
doc.save(base.artifactsDir + "ImageSaveOptions.jpegQuality.HighQuality.jpg", imageOptions);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [ImageSaveOptions](../)

