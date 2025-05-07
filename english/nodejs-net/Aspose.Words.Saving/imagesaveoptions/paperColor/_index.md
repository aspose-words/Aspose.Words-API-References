---
title: ImageSaveOptions.paperColor property
linktitle: paperColor property
articleTitle: paperColor property
second_title: Aspose.Words for Node.js
description: "ImageSaveOptions.paperColor property. Gets or sets the background (paper) color for the generated images"
type: docs
weight: 100
url: /nodejs-net/aspose.words.saving/imagesaveoptions/paperColor/
---

## ImageSaveOptions.paperColor property

Gets or sets the background (paper) color for the generated images.
The default value is white.




```js
get paperColor(): string
```

### Remarks

When rendering pages of a document that specifies its own background color,
then the document background color will override the color specified by this property.




### Examples

Renders a page of a Word document into an image with transparent or colored background.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.font.name = "Times New Roman";
builder.font.size = 24;
builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder.insertImage(base.imageDir + "Logo.jpg");

// Create an "ImageSaveOptions" object which we can pass to the document's "Save" method
// to modify the way in which that method renders the document into an image.
let imgOptions = new aw.Saving.ImageSaveOptions(aw.SaveFormat.Png);
// Set the "PaperColor" property to a transparent color to apply a transparent
// background to the document while rendering it to an image.
imgOptions.paperColor = "rgba(0,0,0,0)";

doc.save(base.artifactsDir + "ImageSaveOptions.paperColor.transparent.png", imgOptions);

// Set the "PaperColor" property to an opaque color to apply that color
// as the background of the document as we render it to an image.
imgOptions.paperColor = "#F08080";

doc.save(base.artifactsDir + "ImageSaveOptions.paperColor.LightCoral.png", imgOptions);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [ImageSaveOptions](../)

