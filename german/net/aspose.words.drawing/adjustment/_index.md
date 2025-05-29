---
title: Adjustment Class
linktitle: Adjustment
articleTitle: Adjustment
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Drawing.Adjustment, die Ihre Formen mit präzisen Anpassungswerten für eine hervorragende Dokumentformatierung verbessert.
type: docs
weight: 700
url: /de/net/aspose.words.drawing/adjustment/
---
## Adjustment class

Stellt Anpassungswerte dar, die auf die angegebene Form angewendet werden.

```csharp
public class Adjustment
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Name](../../aspose.words.drawing/adjustment/name/) { get; } | Ruft den Namen der Anpassung ab. |
| [Value](../../aspose.words.drawing/adjustment/value/) { get; set; } | Ruft den Rohwert der Anpassung ab oder legt ihn fest. |

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
