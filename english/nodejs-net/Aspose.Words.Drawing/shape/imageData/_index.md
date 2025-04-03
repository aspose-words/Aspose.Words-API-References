---
title: Shape.imageData property
linktitle: imageData property
articleTitle: imageData property
second_title: Aspose.Words for NodeJs
description: "Shape.imageData property. Provides access to the image of the shape"
type: docs
weight: 120
url: /nodejs-net/aspose.words.drawing/shape/imageData/
---

## Shape.imageData property

Provides access to the image of the shape.
Returns ``null`` if the shape cannot have an image.



```js
get imageData(): Aspose.Words.Drawing.ImageData
```

### Examples

Shows how to extract images from a document, and save them to the local file system as individual files.

```js
let doc = new aw.Document(base.myDir + "Images.docx");

// Get the collection of shapes from the document,
// and save the image data of every shape with an image as a file to the local file system.
let nodes = [...doc.getChildNodes(aw.NodeType.Shape, true)];

expect(nodes.filter(s => s.asShape().hasImage).length).toEqual(9);

let imageIndex = 0;
for (let node of nodes)
{
  let shape = node.asShape();
  if (shape.hasImage)
  {
    // The image data of shapes may contain images of many possible image formats. 
    // We can determine a file extension for each image automatically, based on its format.
    let imageFileName =
      `File.ExtractImages.${imageIndex}${aw.FileFormatUtil.imageTypeToExtension(shape.imageData.imageType)}`;
    shape.imageData.save(base.artifactsDir + imageFileName);
    imageIndex++;
  }
}
```

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

* module [Aspose.Words.Drawing](../../)
* class [Shape](../)

