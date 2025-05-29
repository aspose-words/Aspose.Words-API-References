---
title: AdjustmentCollection Class
linktitle: AdjustmentCollection
articleTitle: AdjustmentCollection
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Drawing.AdjustmentCollection – din lösning för att hantera skrivskyddade justeringsvärden för former. Förbättra dina dokumentdesigner utan ansträngning!
type: docs
weight: 710
url: /sv/net/aspose.words.drawing/adjustmentcollection/
---
## AdjustmentCollection class

Representerar en skrivskyddad samling av[`Adjustment`](../adjustment/) justera värden som tillämpas på den angivna formen.

```csharp
public class AdjustmentCollection
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Count](../../aspose.words.drawing/adjustmentcollection/count/) { get; } | Hämtar antalet element som finns i samlingen. |
| [Item](../../aspose.words.drawing/adjustmentcollection/item/) { get; } | Returnerar en justering vid det angivna indexet. |

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

* namnutrymme [Aspose.Words.Drawing](../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../)
