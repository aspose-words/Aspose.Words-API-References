---
title: ImageData.ToImage
linktitle: ToImage
articleTitle: ToImage
second_title: Aspose.Words för .NET
description: Lås upp kraften i ToImage-metoden i ImageData för att enkelt hämta bilder lagrade i former som bildobjekt. Förbättra dina projekt utan ansträngning!
type: docs
weight: 230
url: /sv/net/aspose.words.drawing/imagedata/toimage/
---
## ImageData.ToImage method

Hämtar bilden lagrad i formen som enImage objekt.

```csharp
public Image ToImage()
```

## Anmärkningar

En nyImage objektet skapas varje gång den här metoden anropas.

Det är uppringarens ansvar att göra sig av med bildobjektet.

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
