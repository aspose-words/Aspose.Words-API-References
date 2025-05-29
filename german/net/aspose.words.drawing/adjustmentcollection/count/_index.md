---
title: AdjustmentCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „AdjustmentCollection Count“, um einfach die Gesamtzahl der Elemente abzurufen und so die Effizienz Ihrer Datenverwaltung zu steigern.
type: docs
weight: 10
url: /de/net/aspose.words.drawing/adjustmentcollection/count/
---
## AdjustmentCollection.Count property

Ruft die Anzahl der in der Sammlung enthaltenen Elemente ab.

```csharp
public int Count { get; }
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

* class [AdjustmentCollection](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
