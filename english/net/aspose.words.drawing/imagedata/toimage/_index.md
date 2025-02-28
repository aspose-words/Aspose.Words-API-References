---
title: ImageData.ToImage
linktitle: ToImage
articleTitle: ToImage
second_title: Aspose.Words for .NET
description: Unlock the power of the ToImage method in ImageData to easily retrieve images stored in shapes as Image objects. Enhance your projects effortlessly!
type: docs
weight: 230
url: /net/aspose.words.drawing/imagedata/toimage/
---
## ImageData.ToImage method

Gets the image stored in the shape as a Image object.

```csharp
public Image ToImage()
```

## Remarks

A new Image object is created every time this method is called.

It is the responsibility of the caller to dispose the image object.

## Examples

Shows how to save all images from a document to the file system.

```csharp
Document imgSourceDoc = new Document(MyDir + "Images.docx");

// Shapes with the "HasImage" flag set store and display all the document's images.
Shape[] shapesWithImages = imgSourceDoc.GetChildNodes(NodeType.Shape, true).Cast<Shape>()
    .Where(s => s.HasImage).ToArray();

// Go through each shape and save its image.
for (int shapeIndex = 0; shapeIndex < shapesWithImages.Length; ++shapeIndex)
{
    ImageData imageData = shapesWithImages[shapeIndex].ImageData;
    using (FileStream fileStream = File.Create(ArtifactsDir + $"Drawing.SaveAllImages.{shapeIndex + 1}.{imageData.ImageType}"))
        imageData.Save(fileStream);
}
```

### See Also

* class [ImageData](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
