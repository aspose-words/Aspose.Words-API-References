---
title: AdjustmentCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words för .NET
description: Upptäck AdjustmentCollection-objektegenskapen och hämta enkelt justeringar via index för sömlös datahantering och förbättrad prestanda.
type: docs
weight: 20
url: /sv/net/aspose.words.drawing/adjustmentcollection/item/
---
## AdjustmentCollection indexer

Returnerar en justering vid det angivna indexet.

```csharp
public Adjustment this[int index] { get; }
```

| Parameter | Beskrivning |
| --- | --- |
| index | Ett index till samlingen. |

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

* class [Adjustment](../../adjustment/)
* class [AdjustmentCollection](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
