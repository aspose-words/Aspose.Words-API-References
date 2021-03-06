---
title: ImageSize
second_title: Aspose.Words per .NET API Reference
description: Contiene informazioni sulle dimensioni e sulla risoluzione dellimmagine.
type: docs
weight: 940
url: /it/net/aspose.words.drawing/imagesize/
---
## ImageSize class

Contiene informazioni sulle dimensioni e sulla risoluzione dell'immagine.

```csharp
public class ImageSize
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [ImageSize](imagesize#constructor)(int, int) | Inizializza larghezza e altezza sui valori dati in pixel. Inizializza la risoluzione a 96 dpi. |
| [ImageSize](imagesize#constructor_1)(int, int, double, double) | Inizializza larghezza, altezza e risoluzione sui valori indicati. |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [HeightPixels](../../aspose.words.drawing/imagesize/heightpixels) { get; } | Ottiene l'altezza dell'immagine in pixel. |
| [HeightPoints](../../aspose.words.drawing/imagesize/heightpoints) { get; } | Ottiene l'altezza dell'immagine in punti. 1 punto è 1/72 pollici. |
| [HorizontalResolution](../../aspose.words.drawing/imagesize/horizontalresolution) { get; } | Ottiene la risoluzione orizzontale in DPI. |
| [VerticalResolution](../../aspose.words.drawing/imagesize/verticalresolution) { get; } | Ottiene la risoluzione verticale in DPI. |
| [WidthPixels](../../aspose.words.drawing/imagesize/widthpixels) { get; } | Ottiene la larghezza dell'immagine in pixel. |
| [WidthPoints](../../aspose.words.drawing/imagesize/widthpoints) { get; } | Ottiene la larghezza dell'immagine in punti. 1 punto è 1/72 pollici. |

### Esempi

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

            // Quando inseriamo un'immagine utilizzando il metodo "InsertImage", il builder ridimensiona la forma che mostra l'immagine in modo che,
            // quando visualizziamo il documento utilizzando lo zoom del 100% in Microsoft Word, la forma mostra l'immagine nella sua dimensione effettiva.
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);
            Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");

            // Un'immagine 400x400 creerà un oggetto ImageData con una dimensione dell'immagine di 300x300pt.
            ImageSize imageSize = shape.ImageData.ImageSize;

            Assert.AreEqual(300.0d, imageSize.WidthPoints);
            Assert.AreEqual(300.0d, imageSize.HeightPoints);

            // Se le dimensioni di una forma corrispondono alle dimensioni dei dati dell'immagine,
            // quindi la forma mostra l'immagine nella sua dimensione originale.
            Assert.AreEqual(300.0d, shape.Width);
            Assert.AreEqual(300.0d, shape.Height);

             // Riduci le dimensioni complessive della forma del 50%.
            shape.Width *= 0.5;

             // I fattori di ridimensionamento si applicano sia alla larghezza che all'altezza contemporaneamente per preservare le proporzioni della forma.
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

* property [ImageSize](../imagedata/imagesize)
* spazio dei nomi [Aspose.Words.Drawing](../../aspose.words.drawing)
* assemblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
