---
title: Shape.Adjustments
linktitle: Adjustments
articleTitle: Adjustments
second_title: Aspose.Words för .NET
description: Upptäck formjusteringar. Få tillgång till råvärden för exakta formmodifieringar. Förbättra enkelt design med skräddarsydda justeringar för optimala resultat.
type: docs
weight: 20
url: /sv/net/aspose.words.drawing/shape/adjustments/
---
## Shape.Adjustments property

Ger åtkomst till justeringsrådvärdena för en form. För en form som inte innehåller några justeringsrådvärden returnerar den en tom samling.

```csharp
public AdjustmentCollection Adjustments { get; }
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

* class [AdjustmentCollection](../../adjustmentcollection/)
* class [Shape](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
