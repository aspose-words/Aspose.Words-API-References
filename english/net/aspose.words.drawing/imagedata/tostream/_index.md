---
title: ImageData.ToStream
linktitle: ToStream
articleTitle: ToStream
second_title: Aspose.Words for .NET
description: Discover the ImageData ToStream method—efficiently convert images to byte streams for seamless data handling and enhanced application performance.
type: docs
weight: 240
url: /net/aspose.words.drawing/imagedata/tostream/
---
## ImageData.ToStream method

Creates and returns a stream that contains the image bytes.

```csharp
public Stream ToStream()
```

## Remarks

If the image bytes are stored in the shape, creates and returns a MemoryStream object.

If the image is linked and stored in a file, opens the file and returns a FileStream object.

If the image is linked and stored in an external URL, downloads the file and returns a MemoryStream object.

Is it the responsibility of the caller to dispose the stream object.

## Examples

Shows how to create an image file from a shape's raw image data.

```csharp
Document imgSourceDoc = new Document(MyDir + "Images.docx");
Shape imgShape = (Shape) imgSourceDoc.GetChild(NodeType.Shape, 0, true);

Assert.That(imgShape.HasImage, Is.True);

// ToByteArray() returns the array stored in the ImageBytes property.
Assert.That(imgShape.ImageData.ToByteArray(), Is.EqualTo(imgShape.ImageData.ImageBytes));

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
