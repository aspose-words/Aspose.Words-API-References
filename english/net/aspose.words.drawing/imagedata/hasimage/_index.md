---
title: ImageData.HasImage
second_title: Aspose.Words for .NET API Reference
description: ImageData property. Returns true if the shape has image bytes or links an image in C#.
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
IEnumerable<Shape> shapesWithImages = 
    imgSourceDoc.GetChildNodes(NodeType.Shape, true).Cast<Shape>().Where(s => s.HasImage);

// Go through each shape and save its image.
ImageFormatConverter formatConverter = new ImageFormatConverter();

using (IEnumerator<Shape> enumerator = shapesWithImages.GetEnumerator())
{
    int shapeIndex = 0;

    while (enumerator.MoveNext())
    {
        ImageData imageData = enumerator.Current.ImageData;
        ImageFormat format = imageData.ToImage().RawFormat;
        string fileExtension = formatConverter.ConvertToString(format);

        using (FileStream fileStream = File.Create(ArtifactsDir + $"Drawing.SaveAllImages.{++shapeIndex}.{fileExtension}"))
            imageData.Save(fileStream);
    }
}
```

### See Also

* class [ImageData](../)
* namespace [Aspose.Words.Drawing](../../imagedata/)
* assembly [Aspose.Words](../../../)
