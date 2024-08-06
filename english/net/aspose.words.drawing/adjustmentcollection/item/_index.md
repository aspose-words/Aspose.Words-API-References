---
title: AdjustmentCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words for .NET
description: AdjustmentCollection Item property. Returns an adjustment at the specified index in C#.
type: docs
weight: 20
url: /net/aspose.words.drawing/adjustmentcollection/item/
---
## AdjustmentCollection indexer

Returns an adjustment at the specified index.

```csharp
public Adjustment this[int index] { get; }
```

| Parameter | Description |
| --- | --- |
| index | An index into the collection. |

## Examples

Shows how to work with adjustment raw values.

```csharp
Document doc = new Document(MyDir + "Rounded rectangle shape.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

AdjustmentCollection adjustments = shape.Adjustments;
Assert.AreEqual(1, adjustments.Count);

Adjustment adjustment = adjustments[0];
Assert.AreEqual("adj", adjustment.Name);
Assert.AreEqual(16667, adjustment.Value);

adjustment.Value = 30000;

doc.Save(ArtifactsDir + "Shape.Adjustments.docx");
```

### See Also

* class [Adjustment](../../adjustment/)
* class [AdjustmentCollection](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
