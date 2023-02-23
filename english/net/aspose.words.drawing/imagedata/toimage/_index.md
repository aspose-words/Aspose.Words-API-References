---
title: ImageData.ToImage
linktitle: ToImage
second_title: Aspose.Words for .NET API Reference
description: ImageData method. Gets the image stored in the shape as a Image object in C#.
type: docs
weight: 220
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
