---
title: DocumentBuilder.insertNode method
linktitle: insertNode method
articleTitle: insertNode method
second_title: Aspose.Words for NodeJs
description: "DocumentBuilder.insertNode method. Inserts a node before the cursor."
type: docs
weight: 410
url: /nodejs-net/aspose.words/documentbuilder/insertNode/
---

## insertNode(node) {#node}

Inserts a node before the cursor.


```js
insertNode(node: Aspose.Words.Node)
```

| Parameter | Type | Description |
| --- | --- | --- |
| node | [Node](../../node/) |  |

### Examples

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

### See Also

* module [Aspose.Words](../../)
* class [DocumentBuilder](../)

