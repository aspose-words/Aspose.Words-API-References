---
title: ShadowFormat.Clear
linktitle: Clear
articleTitle: Clear
second_title: Aspose.Words för .NET
description: Återställ enkelt ditt skuggformat med ShadowFormat Clear-metoden. Förbättra din design med ett blankt blad idag!
type: docs
weight: 40
url: /sv/net/aspose.words.drawing/shadowformat/clear/
---
## ShadowFormat.Clear method

Rensar skuggformat.

```csharp
public void Clear()
```

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
