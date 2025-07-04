---
title: Adjustment.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words for .NET
description: Discover the Adjustment Name property to easily access and manage your adjustments for improved efficiency and streamlined workflows.
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
Assert.That(adjustments.Count, Is.EqualTo(1));

Adjustment adjustment = adjustments[0];
Assert.That(adjustment.Name, Is.EqualTo("adj"));
Assert.That(adjustment.Value, Is.EqualTo(16667));

adjustment.Value = 30000;

doc.Save(ArtifactsDir + "Shape.Adjustments.docx");
```

### See Also

* class [Adjustment](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
