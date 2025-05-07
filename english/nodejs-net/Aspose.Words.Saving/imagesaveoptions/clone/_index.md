---
title: ImageSaveOptions.clone method
linktitle: clone method
articleTitle: clone method
second_title: Aspose.Words for Node.js
description: "ImageSaveOptions.clone method. Creates a deep clone of this object."
type: docs
weight: 190
url: /nodejs-net/aspose.words.saving/imagesaveoptions/clone/
---

## clone() {#default}

Creates a deep clone of this object.


```js
clone()
```

### Examples

Shows how to select a bit-per-pixel rate with which to render a document to an image.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.paragraphFormat.style = doc.styles.at("Heading 1");
builder.writeln("Hello world!");
builder.insertImage(base.imageDir + "Logo.jpg");

// When we save the document as an image, we can pass a SaveOptions object to
// select a pixel format for the image that the saving operation will generate.
// Various bit per pixel rates will affect the quality and file size of the generated image.
let imageSaveOptions = new aw.Saving.ImageSaveOptions(aw.SaveFormat.Png);
imageSaveOptions.pixelFormat = imagePixelFormat;

// We can clone ImageSaveOptions instances.
expect(imageSaveOptions.clone()).not.toBe(imageSaveOptions);
expect(imageSaveOptions.clone()).toEqual(imageSaveOptions);

doc.save(base.artifactsDir + "ImageSaveOptions.pixelFormat.png", imageSaveOptions);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [ImageSaveOptions](../)

