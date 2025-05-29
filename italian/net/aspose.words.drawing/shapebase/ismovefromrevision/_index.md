---
title: ShapeBase.IsMoveFromRevision
linktitle: IsMoveFromRevision
articleTitle: IsMoveFromRevision
second_title: Aspose.Words per .NET
description: Scopri la proprietà ShapeBase IsMoveFromRevision in Microsoft Word. Tieni traccia facilmente delle modifiche e identifica con precisione gli oggetti spostati o eliminati.
type: docs
weight: 340
url: /it/net/aspose.words.drawing/shapebase/ismovefromrevision/
---
## ShapeBase.IsMoveFromRevision property

Restituisce`VERO` se questo oggetto è stato spostato (eliminato) in Microsoft Word mentre il monitoraggio delle modifiche era abilitato.

```csharp
public bool IsMoveFromRevision { get; }
```

## Esempi

Mostra come identificare le forme di revisione dello spostamento.

```csharp
// Una revisione di spostamento si verifica quando spostiamo un elemento nel corpo del documento tagliandolo e incollandolo in Microsoft Word mentre
// tracciamento delle modifiche. Se includiamo una forma in linea in un tale movimento di testo, anche quella forma sarà una revisione.
// Copiare e incollare o spostare forme mobili non crea revisioni dello spostamento.
Document doc = new Document(MyDir + "Revision shape.docx");

// Le revisioni di spostamento sono costituite da coppie di revisioni "Sposta da" e "Sposta a". Abbiamo spostato questo documento in una forma,
// ma finché non accettiamo o rifiutiamo la revisione dello spostamento, ci saranno due istanze di quella forma.
Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(2, shapes.Length);

// Questa è la revisione "Sposta a", che è la forma nella sua destinazione di arrivo.
// Se accettiamo la revisione, questa forma di revisione "Sposta a" scomparirà,
// e la forma di revisione "Sposta da" rimarrà.
Assert.False(shapes[0].IsMoveFromRevision);
Assert.True(shapes[0].IsMoveToRevision);

// Questa è la revisione "Sposta da", che è la forma nella sua posizione originale.
// Se accettiamo la revisione, questa forma di revisione "Sposta da" scomparirà,
// e la forma di revisione "Sposta a" rimarrà.
Assert.True(shapes[1].IsMoveFromRevision);
Assert.False(shapes[1].IsMoveToRevision);
```

### Guarda anche

* class [ShapeBase](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
