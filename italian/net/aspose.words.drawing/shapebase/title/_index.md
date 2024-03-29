---
title: ShapeBase.Title
linktitle: Title
articleTitle: Title
second_title: Aspose.Words per .NET
description: ShapeBase Title proprietà. Ottiene o imposta il titolo didascalia delloggetto forma corrente in C#.
type: docs
weight: 530
url: /it/net/aspose.words.drawing/shapebase/title/
---
## ShapeBase.Title property

Ottiene o imposta il titolo (didascalia) dell'oggetto forma corrente.

```csharp
public string Title { get; set; }
```

## Osservazioni

L'impostazione predefinita è una stringa vuota.

Non può essere`nullo`, ma può essere una stringa vuota.

## Esempi

Mostra come impostare il titolo di una forma.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Crea una forma, assegnale un titolo e quindi aggiungila al documento.
Shape shape = new Shape(doc, ShapeType.Cube);
shape.Width = 200;
shape.Height = 200;
shape.Title = "My cube";

builder.InsertNode(shape);

// Quando salviamo un documento con una forma che ha un titolo,
// Aspose.Words memorizzerà quel titolo nel testo alternativo della forma.
doc.Save(ArtifactsDir + "Shape.Title.docx");

doc = new Document(ArtifactsDir + "Shape.Title.docx");
shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

Assert.AreEqual(string.Empty, shape.Title);
Assert.AreEqual("Title: My cube", shape.AlternativeText);
```

### Guarda anche

* class [ShapeBase](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
