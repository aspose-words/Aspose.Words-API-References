---
title: SoftEdgeFormat Class
linktitle: SoftEdgeFormat
articleTitle: SoftEdgeFormat
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Drawing.SoftEdgeFormat per arricchire i tuoi documenti con straordinari effetti di bordi morbidi, per un aspetto professionale.
type: docs
weight: 1710
url: /it/net/aspose.words.drawing/softedgeformat/
---
## SoftEdgeFormat class

Rappresenta la formattazione del bordo sfumato per un oggetto.

```csharp
public class SoftEdgeFormat
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Radius](../../aspose.words.drawing/softedgeformat/radius/) { get; set; } | Ottiene o imposta un valore double che rappresenta la lunghezza del raggio per un effetto bordo morbido in punti (pt). Il valore predefinito è 0.0. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Remove](../../aspose.words.drawing/softedgeformat/remove/)() | Rimuove`SoftEdgeFormat` dall'oggetto padre. |

## Osservazioni

Utilizzare il[`SoftEdge`](../shapebase/softedge/) proprietà per accedere alle proprietà del bordo morbido di un oggetto. Non si creano istanze di`SoftEdgeFormat` classe direttamente.

## Esempi

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

* spazio dei nomi [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../)
