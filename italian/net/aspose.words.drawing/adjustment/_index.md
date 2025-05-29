---
title: Adjustment Class
linktitle: Adjustment
articleTitle: Adjustment
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Drawing.Adjustment, progettata per migliorare le tue forme con valori di regolazione precisi per una formattazione superiore dei documenti.
type: docs
weight: 700
url: /it/net/aspose.words.drawing/adjustment/
---
## Adjustment class

Rappresenta i valori di regolazione applicati alla forma specificata.

```csharp
public class Adjustment
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Name](../../aspose.words.drawing/adjustment/name/) { get; } | Ottiene il nome della regolazione. |
| [Value](../../aspose.words.drawing/adjustment/value/) { get; set; } | Ottiene o imposta il valore grezzo della regolazione. |

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
