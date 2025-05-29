---
title: Adjustment.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words per .NET
description: Scopri la proprietà Nome regolazione per accedere e gestire facilmente le tue regolazioni, per una maggiore efficienza e flussi di lavoro semplificati.
type: docs
weight: 10
url: /it/net/aspose.words.drawing/adjustment/name/
---
## Adjustment.Name property

Ottiene il nome della regolazione.

```csharp
public string Name { get; }
```

## Esempi

Mostra come lavorare con i valori grezzi di regolazione.

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

### Guarda anche

* class [Adjustment](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
