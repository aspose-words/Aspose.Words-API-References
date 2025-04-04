---
title: Shape.hasImage property
linktitle: hasImage property
articleTitle: hasImage property
second_title: Aspose.Words for Node.js
description: "Shape.hasImage property. Returns ``true`` if the shape has image bytes or links an image."
type: docs
weight: 90
url: /nodejs-net/aspose.words.drawing/shape/hasImage/
---

## Shape.hasImage property

Returns ``true`` if the shape has image bytes or links an image.



```js
get hasImage(): boolean
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

Shows how to delete all shapes with images from a document.

```js
let doc = new aw.Document(base.myDir + "Images.docx");
let shapes = doc.getChildNodes(aw.NodeType.Shape, true).toArray().map(node => node.asShape());

expect(shapes.filter(s => s.hasImage).length).toEqual(9);

for (let shape of shapes)
  if (shape.hasImage) 
    shape.remove();

shapes = doc.getChildNodes(aw.NodeType.Shape, true).toArray().map(node => node.asShape());
expect(shapes.filter(s => s.hasImage).length).toEqual(0);
```

### See Also

* module [Aspose.Words.Drawing](../../)
* class [Shape](../)

