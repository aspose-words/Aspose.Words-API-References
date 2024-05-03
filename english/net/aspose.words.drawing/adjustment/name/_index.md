---
title: Adjustment.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words for .NET
description: Adjustment Name property. Gets the name of the adjustment in C#.
type: docs
weight: 10
url: /net/aspose.words.drawing/adjustment/name/
---
## Adjustment.Name property

Gets the name of the adjustment.

```csharp
public string Name { get; }
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

* class [Adjustment](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
