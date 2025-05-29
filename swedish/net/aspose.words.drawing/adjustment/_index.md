---
title: Adjustment Class
linktitle: Adjustment
articleTitle: Adjustment
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Drawing.Adjustment, utformad för att förbättra dina former med exakta justeringsvärden för överlägsen dokumentformatering.
type: docs
weight: 700
url: /sv/net/aspose.words.drawing/adjustment/
---
## Adjustment class

Representerar justeringsvärden som tillämpas på den angivna formen.

```csharp
public class Adjustment
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Name](../../aspose.words.drawing/adjustment/name/) { get; } | Hämtar namnet på justeringen. |
| [Value](../../aspose.words.drawing/adjustment/value/) { get; set; } | Hämtar eller ställer in justeringens råvärde. |

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
