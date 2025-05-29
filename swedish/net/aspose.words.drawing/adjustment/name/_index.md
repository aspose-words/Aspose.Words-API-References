---
title: Adjustment.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Justeringsnamn för att enkelt komma åt och hantera dina justeringar för förbättrad effektivitet och effektiva arbetsflöden.
type: docs
weight: 10
url: /sv/net/aspose.words.drawing/adjustment/name/
---
## Adjustment.Name property

Hämtar namnet på justeringen.

```csharp
public string Name { get; }
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

* class [Adjustment](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
