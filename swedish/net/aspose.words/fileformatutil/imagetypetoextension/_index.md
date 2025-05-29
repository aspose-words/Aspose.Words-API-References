---
title: FileFormatUtil.ImageTypeToExtension
linktitle: ImageTypeToExtension
articleTitle: ImageTypeToExtension
second_title: Aspose.Words för .NET
description: Konvertera Aspose.Words-bildtyper till filändelser utan problem med FileFormatUtil-metoden. Få korrekta filändelser med gemener på några sekunder!
type: docs
weight: 50
url: /sv/net/aspose.words/fileformatutil/imagetypetoextension/
---
## FileFormatUtil.ImageTypeToExtension method

Konverterar ett uppräknat värde av bildtypen Aspose.Words till en filändelse. Den returnerade filändelsen är en liten sträng med en inledande punkt.

```csharp
public static string ImageTypeToExtension(ImageType imageType)
```

### Undantag

| undantag | skick |
| --- | --- |
| ArgumentException | Kastar när det inte går att konvertera. |

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

* enum [ImageType](../../../aspose.words.drawing/imagetype/)
* class [FileFormatUtil](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
