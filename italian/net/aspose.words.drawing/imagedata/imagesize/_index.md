---
title: ImageData.ImageSize
linktitle: ImageSize
articleTitle: ImageSize
second_title: Aspose.Words per .NET
description: Scopri la proprietà ImageSize di ImageData per accedere facilmente ai dettagli essenziali sulle dimensioni e sulla risoluzione delle immagini, per una migliore qualità visiva.
type: docs
weight: 130
url: /it/net/aspose.words.drawing/imagedata/imagesize/
---
## ImageData.ImageSize property

Ottiene le informazioni sulle dimensioni e la risoluzione dell'immagine.

```csharp
public ImageSize ImageSize { get; }
```

## Osservazioni

Se l'immagine è solo collegata e non memorizzata nel documento, restituisce dimensione zero.

## Esempi

Mostra come ridimensionare una forma con un'immagine.

```csharp
// Quando inseriamo un'immagine utilizzando il metodo "InsertImage", il builder ridimensiona la forma che visualizza l'immagine in modo che,
// quando visualizziamo il documento utilizzando lo zoom al 100% in Microsoft Word, la forma visualizza l'immagine nelle sue dimensioni reali.
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");

// Un'immagine 400x400 creerà un oggetto ImageData con una dimensione immagine di 300x300pt.
ImageSize imageSize = shape.ImageData.ImageSize;

Assert.AreEqual(300.0d, imageSize.WidthPoints);
Assert.AreEqual(300.0d, imageSize.HeightPoints);

// Se le dimensioni di una forma corrispondono alle dimensioni dei dati dell'immagine,
// quindi la forma visualizza l'immagine nelle sue dimensioni originali.
Assert.AreEqual(300.0d, shape.Width);
Assert.AreEqual(300.0d, shape.Height);

 // Riduce la dimensione complessiva della forma del 50%.
shape.Width *= 0.5;

 // I fattori di scala si applicano contemporaneamente sia alla larghezza che all'altezza per preservare le proporzioni della forma.
Assert.AreEqual(150.0d, shape.Width);
Assert.AreEqual(150.0d, shape.Height);

// Quando ridimensioniamo la forma, la dimensione dei dati dell'immagine rimane la stessa.
Assert.AreEqual(300.0d, imageSize.WidthPoints);
Assert.AreEqual(300.0d, imageSize.HeightPoints);

// Possiamo fare riferimento alle dimensioni dei dati dell'immagine per applicare un ridimensionamento in base alle dimensioni dell'immagine.
shape.Width = imageSize.WidthPoints * 1.1;

Assert.AreEqual(330.0d, shape.Width);
Assert.AreEqual(330.0d, shape.Height);

doc.Save(ArtifactsDir + "Image.ScaleImage.docx");
```

### Guarda anche

* class [ImageSize](../../imagesize/)
* class [ImageData](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
