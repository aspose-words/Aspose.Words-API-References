---
title: ImageData.ToStream
linktitle: ToStream
articleTitle: ToStream
second_title: Aspose.Words för .NET
description: ImageData ToStream metod. Skapar och returnerar en ström som innehåller bildbytes i C#.
type: docs
weight: 230
url: /sv/net/aspose.words.drawing/imagedata/tostream/
---
## ImageData.ToStream method

Skapar och returnerar en ström som innehåller bildbytes.

```csharp
public Stream ToStream()
```

## Anmärkningar

Om bildbytena lagras i formen, skapas och returneras enMemoryStream objekt.

Om bilden är länkad och lagrad i en fil, öppnar filen och returnerar enFileStream objekt.

Om bilden är länkad och lagrad i en extern URL, laddar ned filen och returnerar enMemoryStream objekt.

Är det uppringarens ansvar att kassera strömobjektet.

## Exempel

Visar hur man skapar en bildfil från en forms råa bilddata.

```csharp
Document imgSourceDoc = new Document(MyDir + "Images.docx");
Shape imgShape = (Shape) imgSourceDoc.GetChild(NodeType.Shape, 0, true);

Assert.True(imgShape.HasImage);

// ToByteArray() returnerar arrayen som är lagrad i egenskapen ImageBytes.
Assert.AreEqual(imgShape.ImageData.ImageBytes, imgShape.ImageData.ToByteArray());

// Spara formens bilddata till en bildfil i det lokala filsystemet.
using (Stream imgStream = imgShape.ImageData.ToStream())
{
    using (FileStream outStream = new FileStream(ArtifactsDir + "Drawing.GetDataFromImage.png",
        FileMode.Create, FileAccess.ReadWrite))
    {
        imgStream.CopyTo(outStream);
    }
}
```

### Se även

* class [ImageData](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
