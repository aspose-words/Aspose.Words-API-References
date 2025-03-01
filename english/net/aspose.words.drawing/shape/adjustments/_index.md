---
title: Shape.Adjustments
linktitle: Adjustments
articleTitle: Adjustments
second_title: Aspose.Words for .NET
description: Discover Shape Adjustments. Access raw values for precise shape modifications. Easily enhance designs with tailored adjustments for optimal results.
type: docs
weight: 20
url: /net/aspose.words.drawing/shape/adjustments/
---
## Shape.Adjustments property

Provides access to the adjustment raw values of a shape. For a shape that does not contain any adjustment raw values, it returns an empty collection.

```csharp
public AdjustmentCollection Adjustments { get; }
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

* class [AdjustmentCollection](../../adjustmentcollection/)
* class [Shape](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
