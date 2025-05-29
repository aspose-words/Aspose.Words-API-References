---
title: ShadowFormat.Visible
linktitle: Visible
articleTitle: Visible
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Synlig skuggformat. Kontrollera enkelt om din formatering är synlig, vilket förbättrar ditt dokuments utseende och tydlighet.
type: docs
weight: 30
url: /sv/net/aspose.words.drawing/shadowformat/visible/
---
## ShadowFormat.Visible property

Returer`sann` om formateringen som tillämpats på den här instansen är synlig.

```csharp
public bool Visible { get; }
```

## Anmärkningar

Ogilla[`Clear`](../clear/) , tilldela`falsk`till Synlig rensar inte formateringen, den döljer bara formeffekten.

## Exempel

Visar hur man arbetar med skuggformatering för formen.

```csharp
Document doc = new Document(MyDir + "Shape stroke pattern border.docx");
Shape shape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];

if (shape.ShadowFormat.Visible && shape.ShadowFormat.Type == ShadowType.Shadow2)
    shape.ShadowFormat.Type = ShadowType.Shadow7;

if (shape.ShadowFormat.Type == ShadowType.ShadowMixed)
    shape.ShadowFormat.Clear();
```

### Se även

* class [ShadowFormat](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
