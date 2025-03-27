---
title: ImageBinarizationMethod enumeration
linktitle: ImageBinarizationMethod enumeration
articleTitle: ImageBinarizationMethod enumeration
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Saving.ImageBinarizationMethod enumeration. Specifies the method used to binarize image."
type: docs
weight: 360
url: /nodejs-net/Aspose.Words.Saving/imagebinarizationmethod/
---

## ImageBinarizationMethod enumeration

Specifies the method used to binarize image.


### Members

| Name | Description |
| --- | --- |
| Threshold | Specifies threshold method. |
| FloydSteinbergDithering | Specifies dithering using Floyd-Steinberg error diffusion method. |

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

* module [Aspose.Words.Saving](../)

