---
title: Adjustment.Value
linktitle: Value
articleTitle: Value
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Justeringsvärde, hämta eller ställ enkelt in råa justeringsvärden för att förbättra din datahantering och effektivisera dina processer.
type: docs
weight: 20
url: /sv/net/aspose.words.drawing/adjustment/value/
---
## Adjustment.Value property

Hämtar eller ställer in justeringens råvärde.

```csharp
public int Value { get; set; }
```

## Anmärkningar

Ett justeringsvärde är helt enkelt en guide som har en specificerad värdebaserad formel. Det vill säga, ingen beräkning sker för en justeringsvärdesguide. Istället anger denna guide ett parametervärde som används för beräkningar inom formguiderna.

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

* class [Adjustment](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
