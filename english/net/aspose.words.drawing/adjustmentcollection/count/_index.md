---
title: AdjustmentCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words for .NET
description: Discover the AdjustmentCollection Count property to easily retrieve the total number of elements, enhancing your data management efficiency.
type: docs
weight: 10
url: /net/aspose.words.drawing/adjustmentcollection/count/
---
## AdjustmentCollection.Count property

Gets the number of elements contained in the collection.

```csharp
public int Count { get; }
```

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

* class [AdjustmentCollection](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
