---
title: ImageData.FitImageToShape
linktitle: FitImageToShape
articleTitle: FitImageToShape
second_title: Aspose.Words per .NET
description: Ottimizza le tue immagini con il metodo FitImageToShape, assicurando un perfetto allineamento delle proporzioni all'interno dei riquadri Shape per presentazioni visive straordinarie.
type: docs
weight: 190
url: /it/net/aspose.words.drawing/imagedata/fitimagetoshape/
---
## ImageData.FitImageToShape method

Adatta i dati dell'immagine alla cornice di forma in modo che le proporzioni dei dati dell'immagine corrispondano alle proporzioni della cornice di forma.

```csharp
public void FitImageToShape()
```

## Esempi

Mostra come adattare i dati dell'immagine alla cornice della forma.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisce una forma immagine e lascia il suo orientamento nello stato predefinito.
Shape shape = builder.InsertShape(ShapeType.Rectangle, 300, 450);
shape.ImageData.SetImage(ImageDir + "Barcode.png");
shape.ImageData.FitImageToShape();

doc.Save(ArtifactsDir + "Shape.FitImageToShape.docx");
```

### Guarda anche

* class [ImageData](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
