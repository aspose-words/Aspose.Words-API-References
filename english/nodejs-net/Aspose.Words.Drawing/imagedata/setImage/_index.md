---
title: ImageData.setImage method
linktitle: setImage method
articleTitle: setImage method
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Drawing.ImageData.setImage method"
type: docs
weight: 210
url: /nodejs-net/aspose.words.drawing/imagedata/setImage/
---

## setImage(image) {#jsimage}

```js
setImage(image: Aspose.Words.JSImage)
```

| Parameter | Type | Description |
| --- | --- | --- |
| image | [JSImage](../../../aspose.words/jsimage/) |  |

## setImage(stream) {#buffer}

Sets the image that the shape displays.


```js
setImage(stream: Buffer)
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | Buffer | The stream that contains the image. |

## setImage(fileName) {#string}

Sets the image that the shape displays.


```js
setImage(fileName: string)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fileName | string | The image file. Can be a file name or a URL. |

## Examples

Shows how to insert a linked image into a document.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

const imageFileName = base.imageDir + "Windows MetaFile.wmf";

// Below are two ways of applying an image to a shape so that it can display it.
// 1 -  Set the shape to contain the image.
let shape = new aw.Drawing.Shape(builder.document, aw.Drawing.ShapeType.Image);
shape.wrapType = aw.Drawing.WrapType.Inline;
shape.imageData.setImage(imageFileName);

builder.insertNode(shape);

doc.save(base.artifactsDir + "Image.CreateLinkedImage.embedded.docx");

// Every image that we store in shape will increase the size of our document.
expect(70000 < fs.statSync(base.artifactsDir + "Image.CreateLinkedImage.embedded.docx").size).toBeTruthy();

doc.firstSection.body.firstParagraph.removeAllChildren();

// 2 -  Set the shape to link to an image file in the local file system.
shape = new aw.Drawing.Shape(builder.document, aw.Drawing.ShapeType.Image);
shape.wrapType = aw.Drawing.WrapType.Inline;
shape.imageData.sourceFullName = imageFileName;

builder.insertNode(shape);
doc.save(base.artifactsDir + "Image.CreateLinkedImage.linked.docx");

// Linking to images will save space and result in a smaller document.
// However, the document can only display the image correctly while
// the image file is present at the location that the shape's "SourceFullName" property points to.
expect(10000 > fs.statSync(base.artifactsDir + "Image.CreateLinkedImage.linked.docx").size).toBeTruthy();
```

## See Also

* module [Aspose.Words.Drawing](../../)
* class [ImageData](../)

