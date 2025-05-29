---
title: AdjustmentCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „AdjustmentCollection-Element“ und rufen Sie mühelos Anpassungen nach Index ab, um eine nahtlose Datenverwaltung und verbesserte Leistung zu gewährleisten.
type: docs
weight: 20
url: /de/net/aspose.words.drawing/adjustmentcollection/item/
---
## AdjustmentCollection indexer

Gibt eine Anpassung am angegebenen Index zurück.

```csharp
public Adjustment this[int index] { get; }
```

| Parameter | Beschreibung |
| --- | --- |
| index | Ein Index zur Sammlung. |

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

* class [Adjustment](../../adjustment/)
* class [AdjustmentCollection](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
