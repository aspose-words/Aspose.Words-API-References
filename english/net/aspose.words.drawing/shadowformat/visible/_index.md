---
title: ShadowFormat.Visible
linktitle: Visible
articleTitle: Visible
second_title: Aspose.Words for .NET
description: Discover the ShadowFormat Visible property: Easily check if your formatting is visible, enhancing your document's appearance and clarity.
type: docs
weight: 30
url: /net/aspose.words.drawing/shadowformat/visible/
---
## ShadowFormat.Visible property

Returns `true` if the formatting applied to this instance is visible.

```csharp
public bool Visible { get; }
```

## Remarks

Unlike [`Clear`](../clear/), assigning `false` to Visible does not clear the formatting, it only hides the shape effect.

## Examples

Shows how to work with a shadow formatting for the shape.

```csharp
Document doc = new Document(MyDir + "Shape stroke pattern border.docx");
Shape shape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];

if (shape.ShadowFormat.Visible && shape.ShadowFormat.Type == ShadowType.Shadow2)
    shape.ShadowFormat.Type = ShadowType.Shadow7;

if (shape.ShadowFormat.Type == ShadowType.ShadowMixed)
    shape.ShadowFormat.Clear();
```

### See Also

* class [ShadowFormat](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
