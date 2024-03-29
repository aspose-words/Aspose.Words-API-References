---
title: ImageSize.HeightPoints
linktitle: HeightPoints
articleTitle: HeightPoints
second_title: Aspose.Words per .NET
description: ImageSize HeightPoints proprietà. Ottiene laltezza dellimmagine in punti. 1 punto è 1/72 di pollice in C#.
type: docs
weight: 30
url: /it/net/aspose.words.drawing/imagesize/heightpoints/
---
## ImageSize.HeightPoints property

Ottiene l'altezza dell'immagine in punti. 1 punto è 1/72 di pollice.

```csharp
public double HeightPoints { get; }
```

## Esempi

Mostra come ridimensionare una forma con un'immagine.

```csharp
#if NET48 || JAVA
            Image image = Image.FromFile(ImageDir + "Logo.jpg");

            Assert.AreEqual(400, image.Size.Width);
            Assert.AreEqual(400, image.Size.Height);
#elif NET5_0_OR_GREATER
            SKBitmap image = SKBitmap.Decode(ImageDir + "Logo.jpg");

            Assert.AreEqual(400, image.Width);
            Assert.AreEqual(400, image.Height);
#endif

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
            // la forma visualizza l'immagine nella sua dimensione originale.
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

            // Possiamo fare riferimento alle dimensioni dei dati dell'immagine per applicare un ridimensionamento in base alla dimensione dell'immagine.
            shape.Width = imageSize.WidthPoints * 1.1;

            Assert.AreEqual(330.0d, shape.Width);
            Assert.AreEqual(330.0d, shape.Height);

            doc.Save(ArtifactsDir + "Image.ScaleImage.docx");
```

### Guarda anche

* class [ImageSize](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
