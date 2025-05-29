---
title: AdjustmentCollection Class
linktitle: AdjustmentCollection
articleTitle: AdjustmentCollection
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Drawing.AdjustmentCollection: la tua soluzione per gestire i valori di regolazione in sola lettura per le forme. Migliora la progettazione dei tuoi documenti senza sforzo!
type: docs
weight: 710
url: /it/net/aspose.words.drawing/adjustmentcollection/
---
## AdjustmentCollection class

Rappresenta una raccolta di sola lettura di[`Adjustment`](../adjustment/) regola i valori applicati alla forma specificata.

```csharp
public class AdjustmentCollection
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Count](../../aspose.words.drawing/adjustmentcollection/count/) { get; } | Ottiene il numero di elementi contenuti nella raccolta. |
| [Item](../../aspose.words.drawing/adjustmentcollection/item/) { get; } | Restituisce una regolazione all'indice specificato. |

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

* spazio dei nomi [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../)
