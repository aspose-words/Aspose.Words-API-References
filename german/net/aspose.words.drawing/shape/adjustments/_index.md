---
title: Shape.Adjustments
linktitle: Adjustments
articleTitle: Adjustments
second_title: Aspose.Words für .NET
description: Entdecken Sie Formanpassungen. Greifen Sie auf Rohwerte zu, um präzise Formänderungen vorzunehmen. Optimieren Sie Designs ganz einfach mit maßgeschneiderten Anpassungen für optimale Ergebnisse.
type: docs
weight: 20
url: /de/net/aspose.words.drawing/shape/adjustments/
---
## Shape.Adjustments property

Bietet Zugriff auf die Anpassungsrohwerte einer Form. Für eine Form, die keine Anpassungsrohwerte enthält, wird eine leere Sammlung zurückgegeben.

```csharp
public AdjustmentCollection Adjustments { get; }
```

## Beispiele

Zeigt, wie mit Anpassungsrohwerten gearbeitet wird.

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

### Siehe auch

* class [AdjustmentCollection](../../adjustmentcollection/)
* class [Shape](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
