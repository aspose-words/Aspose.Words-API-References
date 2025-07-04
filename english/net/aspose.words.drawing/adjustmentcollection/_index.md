---
title: AdjustmentCollection Class
linktitle: AdjustmentCollection
articleTitle: AdjustmentCollection
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.Drawing.AdjustmentCollection class—your solution for managing readonly adjustment values for shapes. Enhance your document designs effortlessly!
type: docs
weight: 700
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
Assert.That(adjustments.Count, Is.EqualTo(1));

Adjustment adjustment = adjustments[0];
Assert.That(adjustment.Name, Is.EqualTo("adj"));
Assert.That(adjustment.Value, Is.EqualTo(16667));

adjustment.Value = 30000;

doc.Save(ArtifactsDir + "Shape.Adjustments.docx");
```

### See Also

* namespace [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assembly [Aspose.Words](../../)
