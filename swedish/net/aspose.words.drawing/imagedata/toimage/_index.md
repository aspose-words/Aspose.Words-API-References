---
title: ImageData.ToImage
linktitle: ToImage
articleTitle: ToImage
second_title: Aspose.Words för .NET
description: ImageData ToImage metod. Får bilden lagrad i formen som enImage objekt i C#.
type: docs
weight: 220
url: /sv/net/aspose.words.drawing/imagedata/toimage/
---
## ImageData.ToImage method

Får bilden lagrad i formen som enImage objekt.

```csharp
public Image ToImage()
```

## Anmärkningar

En nyImage objekt skapas varje gång denna metod anropas.

Det är uppringarens ansvar att kassera bildobjektet.

## Exempel

Visar hur man sparar alla bilder från ett dokument till filsystemet.

```csharp
Document imgSourceDoc = new Document(MyDir + "Images.docx");

// Former med flaggan "HasImage" lagrar och visar alla dokumentets bilder.
IEnumerable<Shape> shapesWithImages = 
    imgSourceDoc.GetChildNodes(NodeType.Shape, true).Cast<Shape>().Where(s => s.HasImage);

// Gå igenom varje form och spara dess bild.
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

### Se även

* class [ImageData](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
