---
title: Adjustment.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „Anpassungsname“, um einfach auf Ihre Anpassungen zuzugreifen und sie zu verwalten und so die Effizienz zu verbessern und Arbeitsabläufe zu optimieren.
type: docs
weight: 10
url: /de/net/aspose.words.drawing/adjustment/name/
---
## Adjustment.Name property

Ruft den Namen der Anpassung ab.

```csharp
public string Name { get; }
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

* class [Adjustment](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
