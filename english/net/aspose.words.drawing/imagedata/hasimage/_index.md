---
title: ImageData.HasImage
linktitle: HasImage
articleTitle: HasImage
second_title: Aspose.Words for .NET
description: Discover the ImageData HasImage property: Quickly check if a shape contains image bytes or links, enhancing your design workflow effortlessly.
type: docs
weight: 110
url: /net/aspose.words.drawing/imagedata/hasimage/
---
## ImageData.HasImage property

Returns `true` if the shape has image bytes or links an image.

```csharp
public bool HasImage { get; }
```

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
