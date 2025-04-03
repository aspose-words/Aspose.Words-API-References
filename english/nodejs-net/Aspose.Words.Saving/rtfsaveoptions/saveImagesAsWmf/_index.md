---
title: RtfSaveOptions.saveImagesAsWmf property
linktitle: saveImagesAsWmf property
articleTitle: saveImagesAsWmf property
second_title: Aspose.Words for NodeJs
description: "RtfSaveOptions.saveImagesAsWmf property. When ``true`` all images will be saved as WMF."
type: docs
weight: 50
url: /nodejs-net/aspose.words.saving/rtfsaveoptions/saveImagesAsWmf/
---

## RtfSaveOptions.saveImagesAsWmf property

When ``true`` all images will be saved as WMF.



```js
get saveImagesAsWmf(): boolean
```

### Remarks

This option might help to avoid WordPad warning messages.


### Examples

Shows how to convert all images in a document to the Windows Metafile format as we save the document as an RTF.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.writeln("Jpeg image:");
let imageShape = builder.insertImage(base.imageDir + "Logo.jpg");

expect(imageShape.imageData.imageType).toEqual(aw.Drawing.ImageType.Jpeg);

builder.insertParagraph();
builder.writeln("Png image:");
imageShape = builder.insertImage(base.imageDir + "Transparent background logo.png");

expect(imageShape.imageData.imageType).toEqual(aw.Drawing.ImageType.Png);

// Create an "RtfSaveOptions" object to pass to the document's "Save" method to modify how we save it to an RTF.
let rtfSaveOptions = new aw.Saving.RtfSaveOptions();

// Set the "SaveImagesAsWmf" property to "true" to convert all images in the document to WMF as we save it to RTF.
// Doing so will help readers such as WordPad to read our document.
// Set the "SaveImagesAsWmf" property to "false" to preserve the original format of all images in the document
// as we save it to RTF. This will preserve the quality of the images at the cost of compatibility with older RTF readers.
rtfSaveOptions.saveImagesAsWmf = saveImagesAsWmf;

doc.save(base.artifactsDir + "RtfSaveOptions.saveImagesAsWmf.rtf", rtfSaveOptions);

doc = new aw.Document(base.artifactsDir + "RtfSaveOptions.saveImagesAsWmf.rtf");

let shapes = doc.getChildNodes(aw.NodeType.Shape, true);

if (saveImagesAsWmf)
{
  expect(shapes.at(0).asShape().imageData.imageType).toEqual(aw.Drawing.ImageType.Wmf);
  expect(shapes.at(1).asShape().imageData.imageType).toEqual(aw.Drawing.ImageType.Wmf);
}
else
{
  expect(shapes.at(0).asShape().imageData.imageType).toEqual(aw.Drawing.ImageType.Jpeg);
  expect(shapes.at(1).asShape().imageData.imageType).toEqual(aw.Drawing.ImageType.Png);
}
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [RtfSaveOptions](../)

