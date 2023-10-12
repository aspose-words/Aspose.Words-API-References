---
title: ShapeBase.Width
second_title: Aspose.Words för .NET API Referens
description: ShapeBase fast egendom. Hämtar eller ställer in bredden på formens innehållsblock.
type: docs
weight: 570
url: /sv/net/aspose.words.drawing/shapebase/width/
---
## ShapeBase.Width property

Hämtar eller ställer in bredden på formens innehållsblock.

```csharp
public double Width { get; set; }
```

### Anmärkningar

För en form på toppnivå är värdet i poäng.

För former i en grupp finns värdet i koordinatutrymmet och enheterna för den överordnade gruppen.

Standardvärdet är 0.

### Exempel

Visar hur man infogar en flytande bild och anger dess position och storlek.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;

// Konfigurera formens "RelativeHorizontalPosition"-egenskap för att behandla värdet på egenskapen "Left"
 // som formens horisontella avstånd, i punkter, från sidans vänstra sida.
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;

// Ställ in formens horisontella avstånd från sidans vänstra sida till 100.
shape.Left = 100;

// Använd egenskapen "RelativeVerticalPosition" på liknande sätt för att placera formen 80 pkt under toppen av sidan.
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.Top = 80;

// Ställ in formens höjd, vilket automatiskt skalar bredden för att bevara dimensionerna.
shape.Height = 125;

Assert.AreEqual(125.0d, shape.Width);

// Egenskaperna "Bottom" och "Right" innehåller bildens nedre och högra kanter.
Assert.AreEqual(shape.Top + shape.Height, shape.Bottom);
Assert.AreEqual(shape.Left + shape.Width, shape.Right);

doc.Save(ArtifactsDir + "Image.CreateFloatingPositionSize.docx");
```

Visar hur man ändrar storlek på en form med en bild.

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

            // När vi infogar en bild med metoden "InsertImage" skalar byggaren formen som visar bilden så att,
            // när vi visar dokumentet med 100 % zoom i Microsoft Word, visar formen bilden i dess verkliga storlek.
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);
            Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");

            // En bild på 400x400 skapar ett ImageData-objekt med en bildstorlek på 300x300pt.
            ImageSize imageSize = shape.ImageData.ImageSize;

            Assert.AreEqual(300.0d, imageSize.WidthPoints);
            Assert.AreEqual(300.0d, imageSize.HeightPoints);

            // Om en forms mått matchar bilddatas mått,
            // då visar formen bilden i sin ursprungliga storlek.
            Assert.AreEqual(300.0d, shape.Width);
            Assert.AreEqual(300.0d, shape.Height);

             // Minska formens totala storlek med 50 %.
            shape.Width *= 0.5;

             // Skalningsfaktorer gäller för både bredden och höjden samtidigt för att bevara formens proportioner.
            Assert.AreEqual(150.0d, shape.Width);
            Assert.AreEqual(150.0d, shape.Height);

            // När vi ändrar storlek på formen förblir storleken på bilddata densamma.
            Assert.AreEqual(300.0d, imageSize.WidthPoints);
            Assert.AreEqual(300.0d, imageSize.HeightPoints);

            // Vi kan referera till bilddatadimensionerna för att tillämpa en skalning baserat på bildens storlek.
            shape.Width = imageSize.WidthPoints * 1.1;

            Assert.AreEqual(330.0d, shape.Width);
            Assert.AreEqual(330.0d, shape.Height);

            doc.Save(ArtifactsDir + "Image.ScaleImage.docx");
```

### Se även

* class [ShapeBase](../)
* namnutrymme [Aspose.Words.Drawing](../../shapebase/)
* hopsättning [Aspose.Words](../../../)


