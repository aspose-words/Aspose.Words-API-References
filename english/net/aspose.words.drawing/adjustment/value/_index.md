---
title: Adjustment.Value
linktitle: Value
articleTitle: Value
second_title: Aspose.Words for .NET
description: Discover the Adjustment Value property, easily get or set raw adjustment values to enhance your data management and streamline your processes.
type: docs
weight: 20
url: /net/aspose.words.drawing/adjustment/value/
---
## Adjustment.Value property

Gets or sets the raw value of the adjustment.

```csharp
public int Value { get; set; }
```

## Remarks

An adjust value is simply a guide that has a value based formula specified. That is, no calculation takes place for an adjust value guide. Instead, this guide specifies a parameter value that is used for calculations within the shape guides.

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
