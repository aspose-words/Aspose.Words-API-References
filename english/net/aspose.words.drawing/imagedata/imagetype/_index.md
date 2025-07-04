---
title: ImageData.ImageType
linktitle: ImageType
articleTitle: ImageType
second_title: Aspose.Words for .NET
description: Discover the ImageData ImageType property to easily identify image types and enhance your image handling capabilities. Boost your development efficiency today!
type: docs
weight: 140
url: /net/aspose.words.drawing/imagedata/imagetype/
---
## ImageData.ImageType property

Gets the type of the image.

```csharp
public ImageType ImageType { get; }
```

## Examples

Shows how to extract images from a document, and save them to the local file system as individual files.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Get the collection of shapes from the document,
// and save the image data of every shape with an image as a file to the local file system.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);

Assert.That(shapes.Count(s => ((Shape)s).HasImage), Is.EqualTo(9));

int imageIndex = 0;
foreach (Shape shape in shapes.OfType<Shape>())
{
    if (shape.HasImage)
    {
        // The image data of shapes may contain images of many possible image formats. 
        // We can determine a file extension for each image automatically, based on its format.
        string imageFileName =
            $"File.ExtractImages.{imageIndex}{FileFormatUtil.ImageTypeToExtension(shape.ImageData.ImageType)}";
        shape.ImageData.Save(ArtifactsDir + imageFileName);
        imageIndex++;
    }
}
```

### See Also

* enum [ImageType](../../imagetype/)
* class [ImageData](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
