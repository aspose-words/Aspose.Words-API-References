---
title: ImageData.save method
linktitle: save method
articleTitle: save method
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Drawing.ImageData.save method"
type: docs
weight: 200
url: /nodejs-net/aspose.words.drawing/imagedata/save/
---

## save(stream) {#unknown}

```js
save(stream)
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream |  |  |

## save(fileName) {#string}

Saves the image into a file.


```js
save(fileName: string)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fileName | string | The file name where to save the image. |

## Examples

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

## See Also

* module [Aspose.Words.Drawing](../../)
* class [ImageData](../)

