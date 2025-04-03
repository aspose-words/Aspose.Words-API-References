---
title: FileFormatUtil.imageTypeToExtension method
linktitle: imageTypeToExtension method
articleTitle: imageTypeToExtension method
second_title: Aspose.Words for NodeJs
description: "FileFormatUtil.imageTypeToExtension method. Converts an Aspose.Words image type enumerated value into a file extension"
type: docs
weight: 50
url: /nodejs-net/aspose.words/fileformatutil/imageTypeToExtension/
---

## imageTypeToExtension(imageType) {#imagetype}

Converts an Aspose.Words image type enumerated value into a file extension. The returned extension is a lower-case string with a leading dot.


```js
imageTypeToExtension(imageType: Aspose.Words.Drawing.ImageType)
```

| Parameter | Type | Description |
| --- | --- | --- |
| imageType | [ImageType](../../../aspose.words.drawing/imagetype/) |  |

### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(ArgumentException)) | Throws when cannot convert. |

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

### See Also

* module [Aspose.Words](../../)
* class [FileFormatUtil](../)

