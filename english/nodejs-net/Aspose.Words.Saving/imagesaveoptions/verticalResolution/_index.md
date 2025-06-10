---
title: ImageSaveOptions.verticalResolution property
linktitle: verticalResolution property
articleTitle: verticalResolution property
second_title: Aspose.Words for Node.js
description: "ImageSaveOptions.verticalResolution property. Gets or sets the vertical resolution for the generated images, in dots per inch."
type: docs
weight: 190
url: /nodejs-net/aspose.words.saving/imagesaveoptions/verticalResolution/
---

## ImageSaveOptions.verticalResolution property

Gets or sets the vertical resolution for the generated images, in dots per inch.


```js
get verticalResolution(): number
```

### Remarks

This property has effect only when saving to raster image formats and affects the output size in pixels.

The default value is 96.




### Examples

Shows how to edit the image while Aspose.words converts a document to one.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.paragraphFormat.style = doc.styles.at("Heading 1");
builder.writeln("Hello world!");
builder.insertImage(base.imageDir + "Logo.jpg");

// When we save the document as an image, we can pass a SaveOptions object to
// edit the image while the saving operation renders it.
let options = new aw.Saving.ImageSaveOptions(aw.SaveFormat.Png)
{
  // We can adjust these properties to change the image's brightness and contrast.
  // Both are on a 0-1 scale and are at 0.5 by default.
  ImageBrightness = 0.3f,
  ImageContrast = 0.7f,

  // We can adjust horizontal and vertical resolution with these properties.
  // This will affect the dimensions of the image.
  // The default value for these properties is 96.0, for a resolution of 96dpi.
  HorizontalResolution = 72f,
  VerticalResolution = 72f,

  // We can scale the image using this property. The default value is 1.0, for scaling of 100%.
  // We can use this property to negate any changes in image dimensions that changing the resolution would cause.
  Scale = 96f / 72f
};

doc.save(base.artifactsDir + "ImageSaveOptions.EditImage.png", options);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [ImageSaveOptions](../)

