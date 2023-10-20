---
title: ShapeBase.Height
linktitle: Height
articleTitle: Height
second_title: Aspose.Words per .NET
description: ShapeBase Height proprietà. Ottiene o imposta laltezza del blocco contenitore della forma in C#.
type: docs
weight: 200
url: /it/net/aspose.words.drawing/shapebase/height/
---
## ShapeBase.Height property

Ottiene o imposta l'altezza del blocco contenitore della forma.

```csharp
public double Height { get; set; }
```

## Osservazioni

Per una forma di livello superiore, il valore è in punti.

Per le forme in un gruppo, il valore è nello spazio delle coordinate e nelle unità del gruppo principale.

Il valore predefinito è 0.

## Esempi

Mostra come inserire un'immagine mobile e specificarne la posizione e le dimensioni.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;

// Configura la proprietà "RelativeHorizontalPosition" della forma per trattare il valore della proprietà "Left"
 // come la distanza orizzontale della forma, in punti, dal lato sinistro della pagina.
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;

// Imposta la distanza orizzontale della forma dal lato sinistro della pagina su 100.
shape.Left = 100;

// Utilizza la proprietà "RelativeVerticalPosition" in modo simile per posizionare la forma 80pt sotto la parte superiore della pagina.
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.Top = 80;

// Imposta l'altezza della forma, che ridimensionerà automaticamente la larghezza per preservare le dimensioni.
shape.Height = 125;

Assert.AreEqual(125.0d, shape.Width);

// Le proprietà "Bottom" e "Right" contengono i bordi inferiore e destro dell'immagine.
Assert.AreEqual(shape.Top + shape.Height, shape.Bottom);
Assert.AreEqual(shape.Left + shape.Width, shape.Right);

doc.Save(ArtifactsDir + "Image.CreateFloatingPositionSize.docx");
```

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

* class [ShapeBase](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
