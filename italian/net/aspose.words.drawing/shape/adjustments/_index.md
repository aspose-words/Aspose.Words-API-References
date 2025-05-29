---
title: Shape.Adjustments
linktitle: Adjustments
articleTitle: Adjustments
second_title: Aspose.Words per .NET
description: Scopri le regolazioni di forma. Accedi ai valori grezzi per modifiche precise alla forma. Migliora facilmente i tuoi progetti con regolazioni personalizzate per risultati ottimali.
type: docs
weight: 20
url: /it/net/aspose.words.drawing/shape/adjustments/
---
## Shape.Adjustments property

Fornisce l'accesso ai valori grezzi di regolazione di una forma. Per una forma che non contiene valori grezzi di regolazione, restituisce una raccolta vuota.

```csharp
public AdjustmentCollection Adjustments { get; }
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

* class [AdjustmentCollection](../../adjustmentcollection/)
* class [Shape](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
