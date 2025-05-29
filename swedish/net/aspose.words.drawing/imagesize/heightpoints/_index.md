---
title: ImageSize.HeightPoints
linktitle: HeightPoints
articleTitle: HeightPoints
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ImageSize HeightPoints för att enkelt hämta bildhöjd i punkter – 1 punkt är lika med 1/72 tum. Optimera dina bilder utan ansträngning!
type: docs
weight: 30
url: /sv/net/aspose.words.drawing/imagesize/heightpoints/
---
## ImageSize.HeightPoints property

Hämtar bildens höjd i punkter. 1 punkt är 1/72 tum.

```csharp
public double HeightPoints { get; }
```

## Exempel

Visar hur man ändrar storlek på en form med en bild.

```csharp
// När vi infogar en bild med metoden "InsertImage" skalar byggaren formen som visar bilden så att,
// när vi visar dokumentet med 100 % zoom i Microsoft Word, visar formen bilden i sin verkliga storlek.
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");

// En bild på 400x400 skapar ett ImageData-objekt med en bildstorlek på 300x300pt.
ImageSize imageSize = shape.ImageData.ImageSize;

Assert.AreEqual(300.0d, imageSize.WidthPoints);
Assert.AreEqual(300.0d, imageSize.HeightPoints);

// Om en forms dimensioner matchar bilddatans dimensioner,
// då visar formen bilden i sin ursprungliga storlek.
Assert.AreEqual(300.0d, shape.Width);
Assert.AreEqual(300.0d, shape.Height);

 // Minska formens totala storlek med 50 %.
shape.Width *= 0.5;

 // Skalningsfaktorer gäller för både bredden och höjden samtidigt för att bevara formens proportioner.
Assert.AreEqual(150.0d, shape.Width);
Assert.AreEqual(150.0d, shape.Height);

// När vi ändrar storleken på formen förblir storleken på bilddata densamma.
Assert.AreEqual(300.0d, imageSize.WidthPoints);
Assert.AreEqual(300.0d, imageSize.HeightPoints);

// Vi kan referera till bilddatadimensionerna för att tillämpa en skalning baserad på bildens storlek.
shape.Width = imageSize.WidthPoints * 1.1;

Assert.AreEqual(330.0d, shape.Width);
Assert.AreEqual(330.0d, shape.Height);

doc.Save(ArtifactsDir + "Image.ScaleImage.docx");
```

### Se även

* class [ImageSize](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
