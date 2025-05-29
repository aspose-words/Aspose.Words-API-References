---
title: ImageSize.HeightPixels
linktitle: HeightPixels
articleTitle: HeightPixels
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ImageSize HeightPixels för att enkelt komma åt och optimera bildens höjd i pixlar för bättre prestanda och kvalitet.
type: docs
weight: 20
url: /sv/net/aspose.words.drawing/imagesize/heightpixels/
---
## ImageSize.HeightPixels property

Hämtar bildens höjd i pixlar.

```csharp
public int HeightPixels { get; }
```

## Exempel

Visar hur man läser egenskaperna för en bild i en form.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga en form i dokumentet som innehåller en bild hämtad från vårt lokala filsystem.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");

// Om formen innehåller en bild kommer dess ImageData-egenskap att vara giltig,
// och den kommer att innehålla ett ImageSize-objekt.
ImageSize imageSize = shape.ImageData.ImageSize;

// ImageSize-objektet innehåller skrivskyddad information om bilden i formen.
Assert.AreEqual(400, imageSize.HeightPixels);
Assert.AreEqual(400, imageSize.WidthPixels);

const double delta = 0.05;
Assert.AreEqual(95.98d, imageSize.HorizontalResolution, delta);
Assert.AreEqual(95.98d, imageSize.VerticalResolution, delta);

// Vi kan basera formens storlek på storleken på dess bild för att undvika att bilden sträcks ut.
shape.Width = imageSize.WidthPoints * 2;
shape.Height = imageSize.HeightPoints * 2;

doc.Save(ArtifactsDir + "Drawing.ImageSize.docx");
```

### Se även

* class [ImageSize](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
