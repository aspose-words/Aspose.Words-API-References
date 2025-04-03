---
title: ImagePixelFormat enumeration
linktitle: ImagePixelFormat enumeration
articleTitle: ImagePixelFormat enumeration
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Saving.ImagePixelFormat enumeration. Specifies the pixel format for the generated images of document pages."
type: docs
weight: 380
url: /nodejs-net/aspose.words.saving/imagepixelformat/
---

## ImagePixelFormat enumeration

Specifies the pixel format for the generated images of document pages.


### Members

| Name | Description |
| --- | --- |
| Format16BppRgb555 | 16 bits per pixel, RGB. |
| Format16BppRgb565 | 16 bits per pixel, RGB. |
| Format16BppArgb1555 | 16 bits per pixel, ARGB. |
| Format24BppRgb | 24 bits per pixel, RGB. |
| Format32BppRgb | 32 bits per pixel, RGB. |
| Format32BppArgb | 32 bits per pixel, ARGB. |
| Format32BppPArgb | 32 bits per pixel, ARGB, premultiplied alpha. |
| Format48BppRgb | 48 bits per pixel, RGB. |
| Format64BppArgb | 64 bits per pixel, ARGB. |
| Format64BppPArgb | 64 bits per pixel, ARGB, premultiplied alpha. |
| Format1bppIndexed | 1 bit per pixel, Indexed. |

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

* module [Aspose.Words.Saving](../)

