---
title: AdjustmentCollection Class
linktitle: AdjustmentCollection
articleTitle: AdjustmentCollection
second_title: Aspose.Words for .NET
description: Aspose.Words.Drawing.AdjustmentCollection class. Represents a readonly collection of Adjustment adjust values that are applied to the specified shape in C#.
type: docs
weight: 580
url: /net/aspose.words.drawing/adjustmentcollection/
---
## AdjustmentCollection class

Represents a read-only collection of [`Adjustment`](../adjustment/) adjust values that are applied to the specified shape.

```csharp
public class AdjustmentCollection
```

## Properties

| Name | Description |
| --- | --- |
| [Count](../../aspose.words.drawing/adjustmentcollection/count/) { get; } | Gets the number of elements contained in the collection. |
| [Item](../../aspose.words.drawing/adjustmentcollection/item/) { get; } | Returns an adjustment at the specified index. |

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

* namespace [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assembly [Aspose.Words](../../)
