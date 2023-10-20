---
title: ImageData.ImageBytes
linktitle: ImageBytes
articleTitle: ImageBytes
second_title: Aspose.Words för .NET
description: ImageData ImageBytes fast egendom. Hämtar eller ställer in råbyte för bilden som lagras i formen i C#.
type: docs
weight: 120
url: /sv/net/aspose.words.drawing/imagedata/imagebytes/
---
## ImageData.ImageBytes property

Hämtar eller ställer in råbyte för bilden som lagras i formen.

```csharp
public byte[] ImageBytes { get; set; }
```

## Anmärkningar

Ställer in värdet till`null` eller en tom array tar bort bilden från formen.

Returnerar`null` om bilden inte finns lagrad i dokumentet (t.ex. är bilden troligen länkad i detta fall).

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
