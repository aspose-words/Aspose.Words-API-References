---
title: ShadowFormat.Clear
linktitle: Clear
articleTitle: Clear
second_title: Aspose.Words for .NET API Reference
description: ShadowFormat Clear method. Clears shadow format in C#.
type: docs
weight: 30
url: /net/aspose.words.drawing/shadowformat/clear/
---
## ShadowFormat.Clear method

Clears shadow format.

```csharp
public void Clear()
```

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
* namespace [Aspose.Words.Drawing](../../shadowformat/)
* assembly [Aspose.Words](../../../)
