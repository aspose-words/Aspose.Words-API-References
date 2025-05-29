---
title: ShapeBase.AspectRatioLocked
linktitle: AspectRatioLocked
articleTitle: AspectRatioLocked
second_title: Aspose.Words per .NET
description: Scopri la proprietà ShapeBase AspectRatioLocked per mantenere senza sforzo le proporzioni delle tue forme e ottenere design perfetti. Migliora i tuoi progetti oggi stesso!
type: docs
weight: 40
url: /it/net/aspose.words.drawing/shapebase/aspectratiolocked/
---
## ShapeBase.AspectRatioLocked property

Specifica se le proporzioni della forma sono bloccate.

```csharp
public bool AspectRatioLocked { get; set; }
```

## Osservazioni

Il valore predefinito dipende da[`ShapeType`](../../shapetype/) , per ilImage è`VERO` ma per gli altri tipi di forma è`falso`.

Ha effetto solo sulle forme di livello superiore.

## Esempi

Mostra come bloccare/sbloccare le proporzioni di una forma.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisci una forma. Se apriamo questo documento in Microsoft Word, possiamo fare clic con il pulsante sinistro del mouse sulla forma per visualizzarla.
// otto maniglie di ridimensionamento lungo il perimetro, su cui possiamo cliccare e trascinare per modificarne le dimensioni.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");

// Imposta la proprietà "AspectRatioLocked" su "true" per preservare le proporzioni della forma
// quando si utilizza una qualsiasi delle quattro maniglie di ridimensionamento diagonali, che modificano sia l'altezza che la larghezza dell'immagine.
// L'utilizzo di qualsiasi maniglia di dimensionamento ortogonale che modifichi l'altezza o la larghezza modificherà comunque le proporzioni.
// Imposta la proprietà "AspectRatioLocked" su "false" per consentirci di
// modifica liberamente le proporzioni dell'immagine con tutti i quadratini di ridimensionamento.
shape.AspectRatioLocked = lockAspectRatio;

doc.Save(ArtifactsDir + "Shape.AspectRatio.docx");
```

### Guarda anche

* class [ShapeBase](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
