---
title: ShapeBase.IsDeleteRevision
second_title: Aspose.Words per .NET API Reference
description: ShapeBase proprietà. Restituisce vero se questo oggetto è stato eliminato in Microsoft Word mentre era abilitato il rilevamento delle modifiche.
type: docs
weight: 250
url: /it/net/aspose.words.drawing/shapebase/isdeleterevision/
---
## ShapeBase.IsDeleteRevision property

Restituisce vero se questo oggetto è stato eliminato in Microsoft Word mentre era abilitato il rilevamento delle modifiche.

```csharp
public bool IsDeleteRevision { get; }
```

### Esempi

Mostra come lavorare con le forme di revisione.

```csharp
Document doc = new Document();

Assert.False(doc.TrackRevisions);

// Inserisci una forma in linea senza tenere traccia delle revisioni, il che renderà questa forma non una revisione di alcun tipo.
Shape shape = new Shape(doc, ShapeType.Cube);
shape.WrapType = WrapType.Inline;
shape.Width = 100.0;
shape.Height = 100.0;
doc.FirstSection.Body.FirstParagraph.AppendChild(shape);

// Inizia a tenere traccia delle revisioni e quindi inserisce un'altra forma, che sarà una revisione.
doc.StartTrackRevisions("John Doe");

shape = new Shape(doc, ShapeType.Sun);
shape.WrapType = WrapType.Inline;
shape.Width = 100.0;
shape.Height = 100.0;
doc.FirstSection.Body.FirstParagraph.AppendChild(shape);

Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(2, shapes.Length);

shapes[0].Remove();

// Dato che abbiamo rimosso quella forma mentre stavamo monitorando le modifiche,
// la forma persiste nel documento e conta come una revisione di eliminazione.
// Accettare questa revisione rimuoverà la forma in modo permanente, mentre rifiutandola la manterrà nel documento.
Assert.AreEqual(ShapeType.Cube, shapes[0].ShapeType);
Assert.True(shapes[0].IsDeleteRevision);

// E abbiamo inserito un'altra forma durante il monitoraggio delle modifiche, in modo che quella forma venga conteggiata come una revisione di inserimento.
// Accettare questa revisione assimilerà questa forma nel documento come una non revisione,
// e rifiutare la revisione rimuoverà questa forma in modo permanente.
Assert.AreEqual(ShapeType.Sun, shapes[1].ShapeType);
Assert.True(shapes[1].IsInsertRevision);
```

### Guarda anche

* class [ShapeBase](../)
* spazio dei nomi [Aspose.Words.Drawing](../../shapebase/)
* assemblea [Aspose.Words](../../../)


