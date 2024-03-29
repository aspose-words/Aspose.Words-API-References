---
title: ShapeBase.AspectRatioLocked
linktitle: AspectRatioLocked
articleTitle: AspectRatioLocked
second_title: Aspose.Words per .NET
description: ShapeBase AspectRatioLocked proprietà. Specifica se le proporzioni della forma sono bloccate in C#.
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

Il valore predefinito dipende da[`ShapeType`](../../shapetype/) , per ilImage è`VERO` ma per gli altri tipi di forma lo è`falso`.

Ha effetto solo per le forme di livello superiore.

## Esempi

Mostra come bloccare/sbloccare le proporzioni di una forma.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisci una forma. Se apriamo questo documento in Microsoft Word, possiamo fare clic con il tasto sinistro del mouse sulla forma per rivelarla
// otto maniglie di ridimensionamento attorno al suo perimetro, su cui possiamo fare clic e trascinare per modificarne le dimensioni.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");

// Imposta la proprietà "AspectRatioLocked" su "true" per preservare le proporzioni della forma
// quando si utilizza una delle quattro maniglie di ridimensionamento diagonale, che modificano sia l'altezza che la larghezza dell'immagine.
// L'utilizzo di maniglie di ridimensionamento ortogonali che modificano l'altezza o la larghezza modificherà comunque le proporzioni.
// Imposta la proprietà "AspectRatioLocked" su "false" per permettercelo
// modifica liberamente le proporzioni dell'immagine con tutte le maniglie di ridimensionamento.
shape.AspectRatioLocked = lockAspectRatio;

doc.Save(ArtifactsDir + "Shape.AspectRatio.docx");
```

### Guarda anche

* class [ShapeBase](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
