---
title: ImageData.ImageBytes
linktitle: ImageBytes
articleTitle: ImageBytes
second_title: Aspose.Words for .NET
description: Discover the ImageData ImageBytes property to easily manage and manipulate raw image bytes within your shapes for enhanced visual content.
type: docs
weight: 120
url: /net/aspose.words.drawing/imagedata/imagebytes/
---
## ImageData.ImageBytes property

Gets or sets the raw bytes of the image stored in the shape.

```csharp
public byte[] ImageBytes { get; set; }
```

## Remarks

Setting the value to `null` or an empty array will remove the image from the shape.

Returns `null` if the image is not stored in the document (e.g the image is probably linked in this case).

## Examples

Shows how to create an image file from a shape's raw image data.

```csharp
Document imgSourceDoc = new Document(MyDir + "Images.docx");
Shape imgShape = (Shape) imgSourceDoc.GetChild(NodeType.Shape, 0, true);

Assert.True(imgShape.HasImage);

// ToByteArray() returns the array stored in the ImageBytes property.
Assert.AreEqual(imgShape.ImageData.ImageBytes, imgShape.ImageData.ToByteArray());

// Save the shape's image data to an image file in the local file system.
using (Stream imgStream = imgShape.ImageData.ToStream())
{
    using (FileStream outStream = new FileStream(ArtifactsDir + "Drawing.GetDataFromImage.png",
        FileMode.Create, FileAccess.ReadWrite))
    {
        imgStream.CopyTo(outStream);
    }
}
```

### See Also

* class [ImageData](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
