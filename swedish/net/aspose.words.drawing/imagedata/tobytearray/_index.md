---
title: ImageData.ToByteArray
linktitle: ToByteArray
articleTitle: ToByteArray
second_title: Aspose.Words för .NET
description: Konvertera enkelt vilken bild som helst till en byte-array med ImageData ToByteArray-metoden. Få enkelt tillgång till bildbyte från lagrade eller länkade källor!
type: docs
weight: 220
url: /sv/net/aspose.words.drawing/imagedata/tobytearray/
---
## ImageData.ToByteArray method

Returnerar bildbyte för alla bilder oavsett om bilden är lagrad eller länkad.

```csharp
public byte[] ToByteArray()
```

## Anmärkningar

Om bilden är länkad laddas den ner varje gång den anropas.

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
