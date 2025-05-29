---
title: ShapeBase.Width
linktitle: Width
articleTitle: Width
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ShapeBase Width. Justera enkelt bredden på det block som din form innehåller för ökad designflexibilitet och precision.
type: docs
weight: 610
url: /sv/net/aspose.words.drawing/shapebase/width/
---
## ShapeBase.Width property

Hämtar eller ställer in bredden på det block som innehåller formen.

```csharp
public double Width { get; set; }
```

## Anmärkningar

För en form på översta nivån anges värdet i poäng.

För former i en grupp finns värdet i koordinatrummet och enheterna för den överordnade gruppen.

Standardvärdet är 0.

## Exempel

Visar hur man infogar en flytande bild och anger dess position och storlek.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;

// Konfigurera formens egenskap "RelativeHorizontalPosition" för att behandla värdet för egenskapen "Left"
 // som formens horisontella avstånd, i punkter, från sidans vänstra sida.
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;

// Ställ in formens horisontella avstånd från sidans vänstra sida till 100.
shape.Left = 100;

// Använd egenskapen "RelativeVerticalPosition" på ett liknande sätt för att placera formen 80 pt under sidans överkant.
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.Top = 80;

// Ställ in formens höjd, vilket automatiskt skalar bredden för att bevara måtten.
shape.Height = 125;

Assert.AreEqual(125.0d, shape.Width);

// Egenskaperna "Nedre" och "Höger" innehåller bildens nedre och högra kanter.
Assert.AreEqual(shape.Top + shape.Height, shape.Bottom);
Assert.AreEqual(shape.Left + shape.Width, shape.Right);

doc.Save(ArtifactsDir + "Image.CreateFloatingPositionSize.docx");
```

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

* class [ShapeBase](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
