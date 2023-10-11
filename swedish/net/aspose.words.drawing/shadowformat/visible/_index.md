---
title: ShadowFormat.Visible
second_title: Aspose.Words för .NET API Referens
description: ShadowFormat fast egendom. ReturnerarSann om formateringen som tillämpas på den här instansen är synlig.
type: docs
weight: 20
url: /sv/net/aspose.words.drawing/shadowformat/visible/
---
## ShadowFormat.Visible property

Returnerar`Sann` om formateringen som tillämpas på den här instansen är synlig.

```csharp
public bool Visible { get; }
```

### Anmärkningar

Gillar inte[`Clear`](../clear/) , tilldelar`falsk` to Visible rensar inte formateringen, den döljer bara formeffekten.

### Exempel

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
* namnutrymme [Aspose.Words.Drawing](../../shadowformat/)
* hopsättning [Aspose.Words](../../../)


