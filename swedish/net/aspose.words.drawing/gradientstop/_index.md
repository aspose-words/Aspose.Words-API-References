---
title: GradientStop Class
linktitle: GradientStop
articleTitle: GradientStop
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Drawing.GradientStop, din lösning för att skapa fantastiska gradienter med anpassningsbara stopp för förbättrad dokumentgrafik.
type: docs
weight: 1310
url: /sv/net/aspose.words.drawing/gradientstop/
---
## GradientStop class

Representerar ett gradientstopp.

För att lära dig mer, besök[Arbeta med grafiska element](https://docs.aspose.com/words/net/working-with-graphic-elements/) dokumentationsartikel.

```csharp
public class GradientStop
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [GradientStop](gradientstop/#constructor)(*Color, double*) | Initierar en ny instans av`GradientStop` klass. |
| [GradientStop](gradientstop/#constructor_1)(*Color, double, double*) | Initierar en ny instans av`GradientStop` klass. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [BaseColor](../../aspose.words.drawing/gradientstop/basecolor/) { get; } | Hämtar ett värde som representerar färgen på gradientstoppet utan några modifierare. |
| [Color](../../aspose.words.drawing/gradientstop/color/) { get; set; } | Hämtar eller ställer in ett värde som representerar färgen på gradientstoppet. |
| [Position](../../aspose.words.drawing/gradientstop/position/) { get; set; } | Hämtar eller ställer in ett värde som representerar positionen för ett stopp inom lutningen uttryckt som en procentandel i intervallet 0,0 till 1,0. |
| [Transparency](../../aspose.words.drawing/gradientstop/transparency/) { get; set; } | Hämtar eller ställer in ett värde som representerar transparensen för gradientfyllningen uttryckt som en procentandel i intervallet 0,0 till 1,0. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Remove](../../aspose.words.drawing/gradientstop/remove/)() | Tar bort gradientstoppet från föräldern[`GradientStopCollection`](../gradientstopcollection/) . |

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

* namnutrymme [Aspose.Words.Drawing](../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../)
