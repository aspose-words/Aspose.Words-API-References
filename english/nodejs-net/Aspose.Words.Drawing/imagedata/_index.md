---
title: ImageData class
linktitle: ImageData class
articleTitle: ImageData class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Drawing.ImageData class. Adapts [ImageData](./) class public API for Node.js porting."
type: docs
weight: 210
url: /nodejs-net/aspose.words.drawing/imagedata/
---

## ImageData class

Adapts [ImageData](./) class public API for Node.js porting.



### Remarks

Use the [Shape.imageData](../shape/imageData/) property to access and modify the image inside a shape.
You do not create instances of the [ImageData](./) class directly.

An image can be stored inside a shape, linked to external file or both (linked and stored in the document).

Regardless of whether the image is stored inside the shape or linked, you can always access the actual
image using the [ImageData.toByteArray()](./toByteArray/#default),  or[ImageData.save()](./save/#string) methods.
If the image is stored inside the shape, you can also directly access it using the [ImageData.imageBytes](./imageBytes/) property.

To store an image inside a shape use the [ImageData.setImage()](./setImage/#string) method. To link an image to a shape, set the [ImageData.sourceFullName](./sourceFullName/) property.




### Properties

| Name | Description |
| --- | --- |
| [biLevel](./biLevel/) | Determines whether an image will be displayed in black and white. |
| [borders](./borders/) | Gets the collection of borders of the image. Borders only have effect for inline images. |
| [brightness](./brightness/) | Gets or sets the brightness of the picture. The value for this property must be a number from 0.0 (dimmest) to 1.0 (brightest). |
| [chromaKey](./chromaKey/) | Defines the color value of the image that will be treated as transparent. |
| [contrast](./contrast/) | Gets or sets the contrast for the specified picture. The value for this property must be a number from 0.0 (the least contrast) to 1.0 (the greatest contrast). |
| [cropBottom](./cropBottom/) | Defines the fraction of picture removal from the bottom side. |
| [cropLeft](./cropLeft/) | Defines the fraction of picture removal from the left side. |
| [cropRight](./cropRight/) | Defines the fraction of picture removal from the right side. |
| [cropTop](./cropTop/) | Defines the fraction of picture removal from the top side. |
| [grayScale](./grayScale/) | Determines whether a picture will display in grayscale mode. |
| [hasImage](./hasImage/) | Returns ``true`` if the shape has image bytes or links an image. |
| [imageBytes](./imageBytes/) | Gets or sets the raw bytes of the image stored in the shape. |
| [imageSize](./imageSize/) | Gets the information about image size and resolution. |
| [imageType](./imageType/) | Gets the type of the image. |
| [isLink](./isLink/) | Returns ``true`` if the image is linked to the shape (when [ImageData.sourceFullName](./sourceFullName/) is specified). |
| [isLinkOnly](./isLinkOnly/) | Returns ``true`` if the image is linked and not stored in the document. |
| [sourceFullName](./sourceFullName/) | Gets or sets the path and name of the source file for the linked image. |
| [title](./title/) | Defines the title of an image. |

### Methods

| Name | Description |
| --- | --- |
|[ fitImageToShape()](./fitImageToShape/#default) | Fits the image data to Shape frame so that the aspect ratio of the image data matches the aspect ratio of Shape frame. |
|[ save(stream)](./save/#unknown) | Saves the image into the specified stream. |
|[ save(fileName)](./save/#string) | Saves the image into a file. |
|[ setImage(image)](./setImage/#jsimage) |  |
|[ setImage(stream)](./setImage/#buffer) | Sets the image that the shape displays. |
|[ setImage(fileName)](./setImage/#string) | Sets the image that the shape displays. |
|[ toByteArray()](./toByteArray/#default) | Returns image bytes for any image regardless whether the image is stored or linked. |
|[ toImage2()](./toImage2/#default) |  |

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

* module [Aspose.Words.Drawing](../)

