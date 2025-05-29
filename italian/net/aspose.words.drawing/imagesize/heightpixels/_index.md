---
title: ImageSize.HeightPixels
linktitle: HeightPixels
articleTitle: HeightPixels
second_title: Aspose.Words per .NET
description: Scopri la proprietà ImageSize HeightPixels per accedere facilmente all'altezza in pixel della tua immagine e ottimizzarla per ottenere prestazioni e qualità migliori.
type: docs
weight: 20
url: /it/net/aspose.words.drawing/imagesize/heightpixels/
---
## ImageSize.HeightPixels property

Ottiene l'altezza dell'immagine in pixel.

```csharp
public int HeightPixels { get; }
```

## Esempi

Mostra come leggere le proprietà di un'immagine in una forma.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inseriamo nel documento una forma contenente un'immagine presa dal nostro file system locale.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");

// Se la forma contiene un'immagine, la sua proprietà ImageData sarà valida,
// e conterrà un oggetto ImageSize.
ImageSize imageSize = shape.ImageData.ImageSize;

// L'oggetto ImageSize contiene informazioni di sola lettura sull'immagine all'interno della forma.
Assert.AreEqual(400, imageSize.HeightPixels);
Assert.AreEqual(400, imageSize.WidthPixels);

const double delta = 0.05;
Assert.AreEqual(95.98d, imageSize.HorizontalResolution, delta);
Assert.AreEqual(95.98d, imageSize.VerticalResolution, delta);

// Possiamo basare la dimensione della forma sulla dimensione della sua immagine per evitare di allungare quest'ultima.
shape.Width = imageSize.WidthPoints * 2;
shape.Height = imageSize.HeightPoints * 2;

doc.Save(ArtifactsDir + "Drawing.ImageSize.docx");
```

### Guarda anche

* class [ImageSize](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
