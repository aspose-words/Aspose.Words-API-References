---
title: AspectRatioLocked
second_title: Aspose.Words per .NET API Reference
description: Specifica se le proporzioni della forma sono bloccate.
type: docs
weight: 40
url: /it/net/aspose.words.drawing/shapebase/aspectratiolocked/
---
## ShapeBase.AspectRatioLocked property

Specifica se le proporzioni della forma sono bloccate.

```csharp
public bool AspectRatioLocked { get; set; }
```

### Osservazioni

Il valore predefinito dipende da[`ShapeType`](../shapetype) , per ShapeType.Image lo è **VERO** ma per gli altri tipi di forma lo è **falso**.

Ha effetto solo per le forme di livello superiore.

### Esempi

Mostra come bloccare/sbloccare le proporzioni di una forma.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisci una forma. Se apriamo questo documento in Microsoft Word, possiamo fare clic con il pulsante sinistro del mouse sulla forma da rivelare
// otto maniglie di ridimensionamento attorno al suo perimetro, che possiamo fare clic e trascinare per cambiarne le dimensioni.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");

// Imposta la proprietà "AspectRatioLocked" su "true" per preservare le proporzioni della forma
// quando si utilizza una delle quattro maniglie di ridimensionamento diagonale, che modificano sia l'altezza che la larghezza dell'immagine.
// L'uso di qualsiasi maniglia di ridimensionamento ortogonale che modifica l'altezza o la larghezza cambierà comunque le proporzioni.
// Imposta la proprietà "AspectRatioLocked" su "false" per consentirci di farlo
// cambia liberamente le proporzioni dell'immagine con tutte le maniglie di ridimensionamento.
shape.AspectRatioLocked = lockAspectRatio;

doc.Save(ArtifactsDir + "Shape.AspectRatio.docx");
```

### Guarda anche

* class [ShapeBase](../../shapebase)
* spazio dei nomi [Aspose.Words.Drawing](../../shapebase)
* assemblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->