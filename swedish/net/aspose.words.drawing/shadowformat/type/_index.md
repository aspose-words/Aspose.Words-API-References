---
title: ShadowFormat.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words för .NET
description: Utforska egenskapen ShadowFormat Type för att enkelt anpassa dina skuggeffekter. Hämta eller ställ in ShadowType för ökad designflexibilitet.
type: docs
weight: 20
url: /sv/net/aspose.words.drawing/shadowformat/type/
---
## ShadowFormat.Type property

Hämtar eller ställer in det angivna[`ShadowType`](../../shadowtype/) för ShadowFormat.

```csharp
public ShadowType Type { get; set; }
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

* enum [ShadowType](../../shadowtype/)
* class [ShadowFormat](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
