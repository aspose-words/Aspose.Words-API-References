---
title: ImageData.ImageType
linktitle: ImageType
articleTitle: ImageType
second_title: Aspose.Words för .NET
description: Upptäck ImageData ImageType-egenskapen för att enkelt identifiera bildtyper och förbättra dina bildhanteringsmöjligheter. Öka din utvecklingseffektivitet idag!
type: docs
weight: 140
url: /sv/net/aspose.words.drawing/imagedata/imagetype/
---
## ImageData.ImageType property

Hämtar bildens typ.

```csharp
public ImageType ImageType { get; }
```

## Exempel

Visar hur man extraherar bilder från ett dokument och sparar dem i det lokala filsystemet som enskilda filer.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Hämta samlingen av former från dokumentet,
// och spara bilddata för varje form med en bild som en fil till det lokala filsystemet.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);

Assert.AreEqual(9, shapes.Count(s => ((Shape)s).HasImage));

int imageIndex = 0;
foreach (Shape shape in shapes.OfType<Shape>())
{
    if (shape.HasImage)
    {
         // Bilddata för former kan innehålla bilder i många möjliga bildformat.
        // Vi kan automatiskt bestämma filändelsen för varje bild, baserat på dess format.
        string imageFileName =
            $"File.ExtractImages.{imageIndex}{FileFormatUtil.ImageTypeToExtension(shape.ImageData.ImageType)}";
        shape.ImageData.Save(ArtifactsDir + imageFileName);
        imageIndex++;
    }
}
```

### Se även

* enum [ImageType](../../imagetype/)
* class [ImageData](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
