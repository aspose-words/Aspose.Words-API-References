---
title: ShadowFormat.Color
linktitle: Color
articleTitle: Color
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ShadowFormat Color för att anpassa skuggfärgerna i dina designer. Standardinställningen är svart, men släpp lös din kreativitet med livfulla alternativ!
type: docs
weight: 10
url: /sv/net/aspose.words.drawing/shadowformat/color/
---
## ShadowFormat.Color property

Får enColor objektet som representerar färgen för skuggan. Standardvärdet ärBlack .

```csharp
public Color Color { get; }
```

## Exempel

Visar hur man får skuggfärg.

```csharp
Document doc = new Document(MyDir + "Shadow color.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
ShadowFormat shadowFormat = shape.ShadowFormat;

Assert.AreEqual(Color.Red.ToArgb(), shadowFormat.Color.ToArgb());
Assert.AreEqual(ShadowType.ShadowMixed, shadowFormat.Type);
```

### Se även

* class [ShadowFormat](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
