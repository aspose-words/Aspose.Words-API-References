---
title: AdjustmentCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words per .NET
description: Scopri la proprietà AdjustmentCollection Count per recuperare facilmente il numero totale di elementi, migliorando l'efficienza della gestione dei dati.
type: docs
weight: 10
url: /it/net/aspose.words.drawing/adjustmentcollection/count/
---
## AdjustmentCollection.Count property

Ottiene il numero di elementi contenuti nella raccolta.

```csharp
public int Count { get; }
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

* class [AdjustmentCollection](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
