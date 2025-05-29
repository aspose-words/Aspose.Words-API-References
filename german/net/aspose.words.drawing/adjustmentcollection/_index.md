---
title: AdjustmentCollection Class
linktitle: AdjustmentCollection
articleTitle: AdjustmentCollection
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Drawing.AdjustmentCollection – Ihre Lösung für die Verwaltung schreibgeschützter Anpassungswerte für Formen. Optimieren Sie Ihre Dokumentdesigns mühelos!
type: docs
weight: 710
url: /de/net/aspose.words.drawing/adjustmentcollection/
---
## AdjustmentCollection class

Stellt eine schreibgeschützte Sammlung von[`Adjustment`](../adjustment/) Passen Sie Werte an, die auf die angegebene Form angewendet werden.

```csharp
public class AdjustmentCollection
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Count](../../aspose.words.drawing/adjustmentcollection/count/) { get; } | Ruft die Anzahl der in der Sammlung enthaltenen Elemente ab. |
| [Item](../../aspose.words.drawing/adjustmentcollection/item/) { get; } | Gibt eine Anpassung am angegebenen Index zurück. |

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

* namensraum [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Montage [Aspose.Words](../../)
