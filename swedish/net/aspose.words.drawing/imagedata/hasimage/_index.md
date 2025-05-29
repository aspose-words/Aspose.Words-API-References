---
title: ImageData.HasImage
linktitle: HasImage
articleTitle: HasImage
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ImageData HasImage. Kontrollera snabbt om en form innehåller bildbyte eller länkar, vilket enkelt förbättrar ditt designarbetsflöde.
type: docs
weight: 110
url: /sv/net/aspose.words.drawing/imagedata/hasimage/
---
## ImageData.HasImage property

Returer`sann` om formen har bildbyte eller länkar en bild.

```csharp
public bool HasImage { get; }
```

## Exempel

Visar hur man sparar alla bilder från ett dokument till filsystemet.

```csharp
Document imgSourceDoc = new Document(MyDir + "Images.docx");

// Former med flaggan "HasImage" lagrar och visar alla dokumentets bilder.
Shape[] shapesWithImages = imgSourceDoc.GetChildNodes(NodeType.Shape, true).Cast<Shape>()
    .Where(s => s.HasImage).ToArray();

// Gå igenom varje form och spara dess bild.
for (int shapeIndex = 0; shapeIndex < shapesWithImages.Length; ++shapeIndex)
{
    ImageData imageData = shapesWithImages[shapeIndex].ImageData;
    using (FileStream fileStream = File.Create(ArtifactsDir + $"Drawing.SaveAllImages.{shapeIndex + 1}.{imageData.ImageType}"))
        imageData.Save(fileStream);
}
```

### Se även

* class [ImageData](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
