---
title: ImageData.ToByteArray
linktitle: ToByteArray
articleTitle: ToByteArray
second_title: Aspose.Words för .NET
description: ImageData ToByteArray metod. Returnerar bildbyte för alla bilder oavsett om bilden är lagrad eller länkad i C#.
type: docs
weight: 210
url: /sv/net/aspose.words.drawing/imagedata/tobytearray/
---
## ImageData.ToByteArray method

Returnerar bildbyte för alla bilder oavsett om bilden är lagrad eller länkad.

```csharp
public byte[] ToByteArray()
```

## Anmärkningar

Om bilden är länkad, laddar ner bilden varje gång den anropas.

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
