---
title: AdjustmentCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words per .NET
description: Scopri la proprietà AdjustmentCollection Item e recupera senza sforzo le regolazioni in base all'indice, per una gestione dei dati ottimale e prestazioni migliorate.
type: docs
weight: 20
url: /it/net/aspose.words.drawing/adjustmentcollection/item/
---
## AdjustmentCollection indexer

Restituisce una regolazione all'indice specificato.

```csharp
public Adjustment this[int index] { get; }
```

| Parametro | Descrizione |
| --- | --- |
| index | Un indice della collezione. |

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

* class [Adjustment](../../adjustment/)
* class [AdjustmentCollection](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
