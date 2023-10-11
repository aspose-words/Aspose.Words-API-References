---
title: ShapeBase.IsMoveToRevision
second_title: Aspose.Words per .NET API Reference
description: ShapeBase proprietà. RestituisceVERO se questo oggetto è stato spostato inserito in Microsoft Word mentre il rilevamento delle modifiche era abilitato.
type: docs
weight: 330
url: /it/net/aspose.words.drawing/shapebase/ismovetorevision/
---
## ShapeBase.IsMoveToRevision property

Restituisce`VERO` se questo oggetto è stato spostato (inserito) in Microsoft Word mentre il rilevamento delle modifiche era abilitato.

```csharp
public bool IsMoveToRevision { get; }
```

### Esempi

Mostra come identificare le forme di revisione dello spostamento.

```csharp
// Una revisione di spostamento avviene quando spostiamo un elemento nel corpo del documento tagliandolo e incollandolo in Microsoft Word mentre
// tracciamento delle modifiche. Se in tale movimento del testo coinvolgiamo una forma in linea, anche quella forma costituirà una revisione.
// Copiare e incollare o spostare forme fluttuanti non crea revisioni dello spostamento.
Document doc = new Document(MyDir + "Revision shape.docx");

// Le revisioni di spostamento sono costituite da coppie di revisioni "Sposta da" e "Sposta in". Ci siamo spostati in questo documento in una forma,
// ma finché non accettiamo o rifiutiamo la revisione dello spostamento, ci saranno due istanze di quella forma.
Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(2, shapes.Length);

// Questa è la revisione "Sposta in", ovvero la forma alla sua destinazione di arrivo.
// Se accettiamo la revisione, questa forma di revisione "Sposta in" scomparirà,
// e la forma di revisione "Sposta da" rimarrà.
Assert.False(shapes[0].IsMoveFromRevision);
Assert.True(shapes[0].IsMoveToRevision);

// Questa è la revisione "Sposta da", ovvero la forma nella sua posizione originale.
// Se accettiamo la revisione, questa forma di revisione "Sposta da" scomparirà,
// e la forma di revisione "Sposta in" rimarrà.
Assert.True(shapes[1].IsMoveFromRevision);
Assert.False(shapes[1].IsMoveToRevision);
```

### Guarda anche

* class [ShapeBase](../)
* spazio dei nomi [Aspose.Words.Drawing](../../shapebase/)
* assemblea [Aspose.Words](../../../)


