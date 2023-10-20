---
title: ShadowFormat.Clear
linktitle: Clear
articleTitle: Clear
second_title: Aspose.Words för .NET
description: ShadowFormat Clear metod. Rensar skuggformat i C#.
type: docs
weight: 30
url: /sv/net/aspose.words.drawing/shadowformat/clear/
---
## ShadowFormat.Clear method

Rensar skuggformat.

```csharp
public void Clear()
```

## Exempel

Visar hur man arbetar med en skuggformatering för formen.

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
