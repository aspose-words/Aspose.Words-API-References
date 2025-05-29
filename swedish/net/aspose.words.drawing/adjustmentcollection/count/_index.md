---
title: AdjustmentCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words för .NET
description: Upptäck egenskapen AdjustmentCollection Count för att enkelt hämta det totala antalet element och förbättra effektiviteten i din datahantering.
type: docs
weight: 10
url: /sv/net/aspose.words.drawing/adjustmentcollection/count/
---
## AdjustmentCollection.Count property

Hämtar antalet element som finns i samlingen.

```csharp
public int Count { get; }
```

## Exempel

Visar hur man arbetar med justeringsrådvärden.

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

### Se även

* class [AdjustmentCollection](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
