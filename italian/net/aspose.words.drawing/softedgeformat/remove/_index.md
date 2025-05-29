---
title: SoftEdgeFormat.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words per .NET
description: Rimuovi facilmente SoftEdgeFormat dall'oggetto padre con il metodo SoftEdgeFormat Remove. Ottimizza il tuo design per risultati ottimali!
type: docs
weight: 20
url: /it/net/aspose.words.drawing/softedgeformat/remove/
---
## SoftEdgeFormat.Remove method

Rimuove[`SoftEdgeFormat`](../) dall'oggetto padre.

```csharp
public void Remove()
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
