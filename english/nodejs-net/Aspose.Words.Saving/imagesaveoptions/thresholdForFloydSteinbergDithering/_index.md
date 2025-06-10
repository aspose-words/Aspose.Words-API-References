---
title: ImageSaveOptions.thresholdForFloydSteinbergDithering property
linktitle: thresholdForFloydSteinbergDithering property
articleTitle: thresholdForFloydSteinbergDithering property
second_title: Aspose.Words for Node.js
description: "ImageSaveOptions.thresholdForFloydSteinbergDithering property. Gets or sets the threshold that determines the value of the binarization error in the Floyd-Steinberg method"
type: docs
weight: 150
url: /nodejs-net/aspose.words.saving/imagesaveoptions/thresholdForFloydSteinbergDithering/
---

## ImageSaveOptions.thresholdForFloydSteinbergDithering property

Gets or sets the threshold that determines the value
of the binarization error in the Floyd-Steinberg method.
when [ImageBinarizationMethod](../../imagebinarizationmethod/) is [ImageBinarizationMethod.FloydSteinbergDithering](../../imagebinarizationmethod/#FloydSteinbergDithering).



```js
get thresholdForFloydSteinbergDithering(): number
```

### Remarks

The default value is 128.




### Examples

Shows how to set the TIFF binarization error threshold when using the Floyd-Steinberg method to render a TIFF image.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.paragraphFormat.style = doc.styles.at("Heading 1");
builder.writeln("Hello world!");
builder.insertImage(base.imageDir + "Logo.jpg");

// When we save the document as a TIFF, we can pass a SaveOptions object to
// adjust the dithering that Aspose.words will apply when rendering this image.
// The default value of the "ThresholdForFloydSteinbergDithering" property is 128.
// Higher values tend to produce darker images.
let options = new aw.Saving.ImageSaveOptions(aw.SaveFormat.Tiff)
{
  TiffCompression = aw.Saving.TiffCompression.Ccitt3,
  TiffBinarizationMethod = aw.Saving.ImageBinarizationMethod.FloydSteinbergDithering,
  ThresholdForFloydSteinbergDithering = 240
};

doc.save(base.artifactsDir + "ImageSaveOptions.floydSteinbergDithering.tiff", options);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [ImageSaveOptions](../)

