---
title: Fill.GradientStops
linktitle: GradientStops
articleTitle: GradientStops
second_title: Aspose.Words för .NET
description: Upptäck hur du kan förbättra dina designer med egenskapen GradientStops, som innehåller en samling GradientStop-objekt för fantastiska fyllningseffekter.
type: docs
weight: 110
url: /sv/net/aspose.words.drawing/fill/gradientstops/
---
## Fill.GradientStops property

Hämtar en samling av[`GradientStop`](../../gradientstop/) objekt för fyllningen.

```csharp
public GradientStopCollection GradientStops { get; }
```

## Exempel

Visar hur man lägger till övertoningsstopp i övertoningsfyllningen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
shape.Fill.TwoColorGradient(Color.Green, Color.Red, GradientStyle.Horizontal, GradientVariant.Variant2);

// Hämta samling av gradientstopp.
GradientStopCollection gradientStops = shape.Fill.GradientStops;

// Ändra första gradientstopp.
gradientStops[0].Color = Color.Aqua;
gradientStops[0].Position = 0.1;
gradientStops[0].Transparency = 0.25;

// Lägg till nytt gradientstopp i slutet av samlingen.
GradientStop gradientStop = new GradientStop(Color.Brown, 0.5);
gradientStops.Add(gradientStop);

// Ta bort gradientstoppet vid index 1.
gradientStops.RemoveAt(1);
// Och infoga ett nytt gradientstopp vid samma index 1.
gradientStops.Insert(1, new GradientStop(Color.Chocolate, 0.75, 0.3));

// Ta bort sista gradientstoppet i samlingen.
gradientStop = gradientStops[2];
gradientStops.Remove(gradientStop);

Assert.AreEqual(2, gradientStops.Count);

Assert.AreEqual(Color.FromArgb(255, 0, 255, 255), gradientStops[0].BaseColor);
Assert.AreEqual(Color.Aqua.ToArgb(), gradientStops[0].Color.ToArgb());
Assert.AreEqual(0.1d, gradientStops[0].Position, 0.01d);
Assert.AreEqual(0.25d, gradientStops[0].Transparency, 0.01d);

Assert.AreEqual(Color.Chocolate.ToArgb(), gradientStops[1].Color.ToArgb());
Assert.AreEqual(0.75d, gradientStops[1].Position, 0.01d);
Assert.AreEqual(0.3d, gradientStops[1].Transparency, 0.01d);

// Använd alternativet compliance för att definiera formen med DML
// om du vill få egenskapen "GradientStops" efter att dokumentet sparats.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

doc.Save(ArtifactsDir + "Shape.GradientStops.docx", saveOptions);
```

### Se även

* class [GradientStopCollection](../../gradientstopcollection/)
* class [Fill](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
