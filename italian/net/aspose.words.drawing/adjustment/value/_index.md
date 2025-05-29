---
title: Adjustment.Value
linktitle: Value
articleTitle: Value
second_title: Aspose.Words per .NET
description: Scopri la proprietà Valore di aggiustamento, ottieni o imposta facilmente valori di aggiustamento grezzi per migliorare la gestione dei dati e semplificare i processi.
type: docs
weight: 20
url: /it/net/aspose.words.drawing/adjustment/value/
---
## Adjustment.Value property

Ottiene o imposta il valore grezzo della regolazione.

```csharp
public int Value { get; set; }
```

## Osservazioni

Un valore di regolazione è semplicemente una guida in cui è specificata una formula basata sul valore. Vale a dire che non viene eseguito alcun calcolo per una guida al valore di regolazione. Invece, questa guida specifica un valore di parametro che viene utilizzato per i calcoli all'interno delle guide di forma.

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
