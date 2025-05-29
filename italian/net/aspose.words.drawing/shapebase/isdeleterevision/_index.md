---
title: ShapeBase.IsDeleteRevision
linktitle: IsDeleteRevision
articleTitle: IsDeleteRevision
second_title: Aspose.Words per .NET
description: Scopri la proprietà IsDeleteRevision di ShapeBase e scopri come indica l'eliminazione di un oggetto in Microsoft Word con il rilevamento delle modifiche abilitato per una gestione avanzata dei documenti.
type: docs
weight: 270
url: /it/net/aspose.words.drawing/shapebase/isdeleterevision/
---
## ShapeBase.IsDeleteRevision property

Restituisce true se questo oggetto è stato eliminato in Microsoft Word mentre il monitoraggio delle modifiche era abilitato.

```csharp
public bool IsDeleteRevision { get; }
```

## Esempi

Mostra come lavorare con le forme di revisione.

```csharp
Document doc = new Document();

Assert.False(doc.TrackRevisions);

// Inserisci una forma in linea senza tenere traccia delle revisioni, il che farà sì che questa forma non sia una revisione di alcun tipo.
Shape shape = new Shape(doc, ShapeType.Cube);
shape.WrapType = WrapType.Inline;
shape.Width = 100.0;
shape.Height = 100.0;
doc.FirstSection.Body.FirstParagraph.AppendChild(shape);

// Inizia a monitorare le revisioni e poi inserisci un'altra forma, che sarà una revisione.
doc.StartTrackRevisions("John Doe");

shape = new Shape(doc, ShapeType.Sun);
shape.WrapType = WrapType.Inline;
shape.Width = 100.0;
shape.Height = 100.0;
doc.FirstSection.Body.FirstParagraph.AppendChild(shape);

Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(2, shapes.Length);

shapes[0].Remove();

// Poiché abbiamo rimosso quella forma mentre stavamo monitorando le modifiche,
// la forma persiste nel documento e viene conteggiata come una revisione eliminata.
// Accettando questa revisione la forma verrà rimossa in modo permanente, mentre rifiutandola verrà mantenuta nel documento.
Assert.AreEqual(ShapeType.Cube, shapes[0].ShapeType);
Assert.True(shapes[0].IsDeleteRevision);

// E abbiamo inserito un'altra forma durante il monitoraggio delle modifiche, quindi quella forma verrà conteggiata come una revisione inserita.
// L'accettazione di questa revisione assimilerà questa forma al documento come una non-revisione,
// e rifiutando la revisione questa forma verrà rimossa in modo permanente.
Assert.AreEqual(ShapeType.Sun, shapes[1].ShapeType);
Assert.True(shapes[1].IsInsertRevision);
```

### Guarda anche

* class [ShapeBase](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
