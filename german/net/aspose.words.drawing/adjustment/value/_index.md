---
title: Adjustment.Value
linktitle: Value
articleTitle: Value
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „Anpassungswert“. Rufen Sie ganz einfach Rohanpassungswerte ab oder legen Sie sie fest, um Ihr Datenmanagement zu verbessern und Ihre Prozesse zu optimieren.
type: docs
weight: 20
url: /de/net/aspose.words.drawing/adjustment/value/
---
## Adjustment.Value property

Ruft den Rohwert der Anpassung ab oder legt ihn fest.

```csharp
public int Value { get; set; }
```

## Bemerkungen

Ein Anpassungswert ist einfach eine Anleitung, für die eine wertbasierte Formel angegeben ist. Das heißt, für eine Anleitung zum Anpassen von Werten findet keine Berechnung statt. Stattdessen gibt diese Anleitung einen Parameterwert an, der für Berechnungen innerhalb der Formanleitungen verwendet wird.

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
