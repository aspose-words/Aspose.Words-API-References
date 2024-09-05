---
title: Adjustment Class
linktitle: Adjustment
articleTitle: Adjustment
second_title: Aspose.Words for .NET
description: Aspose.Words.Drawing.Adjustment class. Represents adjustment values that are applied to the specified shape in C#.
type: docs
weight: 590
url: /net/aspose.words.drawing/adjustment/
---
## Adjustment class

Represents adjustment values that are applied to the specified shape.

```csharp
public class Adjustment
```

## Properties

| Name | Description |
| --- | --- |
| [Name](../../aspose.words.drawing/adjustment/name/) { get; } | Gets the name of the adjustment. |
| [Value](../../aspose.words.drawing/adjustment/value/) { get; set; } | Gets or sets the raw value of the adjustment. |

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
