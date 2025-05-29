---
title: ShapeBase.Rotation
linktitle: Rotation
articleTitle: Rotation
second_title: Aspose.Words per .NET
description: Scopri la proprietà Rotazione ShapeBase, definisci e personalizza facilmente gli angoli di rotazione delle tue forme, migliorando la precisione e la creatività del tuo design.
type: docs
weight: 500
url: /it/net/aspose.words.drawing/shapebase/rotation/
---
## ShapeBase.Rotation property

Definisce l'angolo (in gradi) di rotazione di una forma. Il valore positivo corrisponde all'angolo di rotazione in senso orario.

```csharp
public double Rotation { get; set; }
```

## Osservazioni

Il valore predefinito è 0.

## Esempi

Mostra come inserire e ruotare un'immagine.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisci una forma con un'immagine.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
Assert.True(shape.CanHaveImage);
Assert.True(shape.HasImage);

// Ruota l'immagine di 45 gradi in senso orario.
shape.Rotation = 45;

doc.Save(ArtifactsDir + "Shape.Rotate.docx");
```

### Guarda anche

* class [ShapeBase](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
