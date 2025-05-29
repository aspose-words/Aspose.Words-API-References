---
title: ShapeBase.IsDecorative
linktitle: IsDecorative
articleTitle: IsDecorative
second_title: Aspose.Words per .NET
description: Scopri ShapeBase. Gestisci facilmente le proprietà decorative nei tuoi documenti. Migliora l'aspetto visivo impostando flag per forme dal design unico.
type: docs
weight: 260
url: /it/net/aspose.words.drawing/shapebase/isdecorative/
---
## ShapeBase.IsDecorative property

Ottiene o imposta il flag che specifica se la forma è decorativa nel documento.

```csharp
public bool IsDecorative { get; set; }
```

## Osservazioni

Nota che la forma non ha spazio vuoto[`AlternativeText`](../alternativetext/) non può essere decorativo.

## Esempi

Mostra come impostare la forma come decorativa.

```csharp
Document doc = new Document(MyDir + "Decorative shapes.docx");

Shape shape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];
Assert.True(shape.IsDecorative);

// Se "AlternativeText" non è vuoto, la forma non può essere decorativa.
// Ecco perché il nostro valore è cambiato in "falso".
shape.AlternativeText = "Alternative text.";
Assert.False(shape.IsDecorative);

DocumentBuilder builder = new DocumentBuilder(doc);

builder.MoveToDocumentEnd();
// Crea una nuova forma decorativa.
shape = builder.InsertShape(ShapeType.Rectangle, 100, 100);
shape.IsDecorative = true;

doc.Save(ArtifactsDir + "Shape.IsDecorative.docx");
```

### Guarda anche

* class [ShapeBase](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
