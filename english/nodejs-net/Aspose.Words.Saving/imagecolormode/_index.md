---
title: ImageColorMode enumeration
linktitle: ImageColorMode enumeration
articleTitle: ImageColorMode enumeration
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Saving.ImageColorMode enumeration. Specifies the color mode for the generated images of document pages."
type: docs
weight: 360
url: /nodejs-net/aspose.words.saving/imagecolormode/
---

## ImageColorMode enumeration

Specifies the color mode for the generated images of document pages.


### Members

| Name | Description |
| --- | --- |
| None | The pages of the document will be rendered as color images. |
| Grayscale | The pages of the document will be rendered as grayscale images. |
| BlackAndWhite | The pages of the document will be rendered as black and white images. |

### Examples

Shows how to set a color mode when rendering documents.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.paragraphFormat.style = doc.styles.at("Heading 1");
builder.writeln("Hello world!");
builder.insertImage(base.imageDir + "Logo.jpg");

// When we save the document as an image, we can pass a SaveOptions object to
// select a color mode for the image that the saving operation will generate.
// If we set the "ImageColorMode" property to "ImageColorMode.BlackAndWhite",
// the saving operation will apply grayscale color reduction while rendering the document.
// If we set the "ImageColorMode" property to "ImageColorMode.Grayscale", 
// the saving operation will render the document into a monochrome image.
// If we set the "ImageColorMode" property to "None", the saving operation will apply the default method
// and preserve all the document's colors in the output image.
let imageSaveOptions = new aw.Saving.ImageSaveOptions(aw.SaveFormat.Png);
imageSaveOptions.imageColorMode = imageColorMode;

doc.save(base.artifactsDir + "ImageSaveOptions.colorMode.png", imageSaveOptions);
```

### See Also

* module [Aspose.Words.Saving](../)

