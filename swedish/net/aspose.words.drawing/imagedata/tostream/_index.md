---
title: ImageData.ToStream
linktitle: ToStream
articleTitle: ToStream
second_title: Aspose.Words för .NET
description: Upptäck ImageData ToStream-metoden – konvertera effektivt bilder till byteströmmar för sömlös datahantering och förbättrad applikationsprestanda.
type: docs
weight: 240
url: /sv/net/aspose.words.drawing/imagedata/tostream/
---
## ImageData.ToStream method

Skapar och returnerar en ström som innehåller bildens byte.

```csharp
public Stream ToStream()
```

## Anmärkningar

Om bildbytena lagras i formen, skapas och returneras enMemoryStream objekt.

Om bilden är länkad och lagrad i en fil öppnas filen och returnerar enFileStream objekt.

Om bilden är länkad och lagrad i en extern URL, laddas filen ner och returnerar enMemoryStream objekt.

Är det anroparens ansvar att kassera strömobjektet.

## Exempel

Visar hur man skapar en bildfil från en forms rådata i bilden.

```csharp
Document imgSourceDoc = new Document(MyDir + "Images.docx");
Shape imgShape = (Shape) imgSourceDoc.GetChild(NodeType.Shape, 0, true);

Assert.True(imgShape.HasImage);

// ToByteArray() returnerar arrayen som lagras i ImageBytes-egenskapen.
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
