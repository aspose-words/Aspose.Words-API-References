---
title: SoftEdgeFormat.Radius
linktitle: Radius
articleTitle: Radius
second_title: Aspose.Words per .NET
description: Scopri la proprietà Raggio SoftEdgeFormat per regolare facilmente gli effetti di smussatura dei bordi. Controlla la lunghezza del raggio con precisione per risultati visivi straordinari.
type: docs
weight: 10
url: /it/net/aspose.words.drawing/softedgeformat/radius/
---
## SoftEdgeFormat.Radius property

Ottiene o imposta un valore double che rappresenta la lunghezza del raggio per un effetto bordo morbido in punti (pt). Il valore predefinito è 0.0.

```csharp
public double Radius { get; set; }
```

## Esempi

Mostra come impostare un limite per la risoluzione dell'immagine.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

SvgSaveOptions saveOptions = new SvgSaveOptions();
saveOptions.MaxImageResolution = 72;

doc.Save(ArtifactsDir + "SvgSaveOptions.MaxImageResolution.svg", saveOptions);
```

Mostra come lavorare con la formattazione soft edge.

```csharp
DocumentBuilder builder = new DocumentBuilder();
Shape shape = builder.InsertShape(ShapeType.Rectangle, 200, 200);

// Applica un bordo morbido alla forma.
shape.SoftEdge.Radius = 30;

builder.Document.Save(ArtifactsDir + "Shape.SoftEdge.docx");

// Carica un documento di forma rettangolare con bordo sfumato.
Document doc = new Document(ArtifactsDir + "Shape.SoftEdge.docx");
shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
SoftEdgeFormat softEdgeFormat = shape.SoftEdge;

// Controlla il raggio del bordo morbido.
Assert.AreEqual(30, softEdgeFormat.Radius);

// Rimuovi il bordo morbido dalla forma.
softEdgeFormat.Remove();

// Controlla il raggio del bordo morbido rimosso.
Assert.AreEqual(0, softEdgeFormat.Radius);
```

### Guarda anche

* class [SoftEdgeFormat](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
