---
title: ShapeBase.SoftEdge
linktitle: SoftEdge
articleTitle: SoftEdge
second_title: Aspose.Words per .NET
description: Migliora i tuoi progetti con ShapeBase SoftEdge per una formattazione fluida e morbida dei bordi. Valorizza i tuoi elementi visivi senza sforzo e distinguiti in ogni progetto!
type: docs
weight: 550
url: /it/net/aspose.words.drawing/shapebase/softedge/
---
## ShapeBase.SoftEdge property

Ottiene la formattazione dei bordi sfumati per la forma.

```csharp
public SoftEdgeFormat SoftEdge { get; }
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

* class [SoftEdgeFormat](../../softedgeformat/)
* class [ShapeBase](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
