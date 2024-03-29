---
title: ShapeBase.IsDecorative
linktitle: IsDecorative
articleTitle: IsDecorative
second_title: Aspose.Words per .NET
description: ShapeBase IsDecorative proprietà. Ottiene o imposta il flag che specifica se la forma è decorativa nel documento in C#.
type: docs
weight: 240
url: /it/net/aspose.words.drawing/shapebase/isdecorative/
---
## ShapeBase.IsDecorative property

Ottiene o imposta il flag che specifica se la forma è decorativa nel documento.

```csharp
public bool IsDecorative { get; set; }
```

## Osservazioni

Nota che la forma non è vuota[`AlternativeText`](../alternativetext/) non può essere decorativo.

## Esempi

Mostra come impostare la forma come decorativa.

```csharp
Document doc = new Document(MyDir + "Decorative shapes.docx");

Shape shape = (Shape) doc.GetChildNodes(NodeType.Shape, true)[0];
Assert.True(shape.IsDecorative);

// Se "AlternativeText" non è vuoto, la forma non può essere decorativa.
// Ecco perché il nostro valore è cambiato in 'false'.
shape.AlternativeText = "Alternative text.";
Assert.False(shape.IsDecorative);

DocumentBuilder builder = new DocumentBuilder(doc);

builder.MoveToDocumentEnd();
// Crea una nuova forma come decorativa.
shape = builder.InsertShape(ShapeType.Rectangle, 100, 100);
shape.IsDecorative = true;

doc.Save(ArtifactsDir + "Shape.IsDecorative.docx");
```

### Guarda anche

* class [ShapeBase](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
