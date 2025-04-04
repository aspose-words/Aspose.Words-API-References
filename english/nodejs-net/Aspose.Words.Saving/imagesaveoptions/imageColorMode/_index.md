---
title: ImageSaveOptions.imageColorMode property
linktitle: imageColorMode property
articleTitle: imageColorMode property
second_title: Aspose.Words for Node.js
description: "ImageSaveOptions.imageColorMode property. Gets or sets the color mode for the generated images."
type: docs
weight: 40
url: /nodejs-net/aspose.words.saving/imagesaveoptions/imageColorMode/
---

## ImageSaveOptions.imageColorMode property

Gets or sets the color mode for the generated images.


```js
get imageColorMode(): Aspose.Words.Saving.ImageColorMode
```

### Remarks

This property has effect only when saving to raster image formats.

The default value is [ImageColorMode.None](../../imagecolormode/#None).




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

* module [Aspose.Words.Saving](../../)
* class [ImageSaveOptions](../)

