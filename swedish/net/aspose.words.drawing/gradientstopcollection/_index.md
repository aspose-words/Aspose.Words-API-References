---
title: GradientStopCollection Class
linktitle: GradientStopCollection
articleTitle: GradientStopCollection
second_title: Aspose.Words för .NET
description: Utforska klassen Aspose.Words.Drawing.GradientStopCollection, med en robust samling anpassningsbara GradientStop-objekt för förbättrad dokumentdesign.
type: docs
weight: 1320
url: /sv/net/aspose.words.drawing/gradientstopcollection/
---
## GradientStopCollection class

Innehåller en samling av[`GradientStop`](../gradientstop/) objekt.

För att lära dig mer, besök[Arbeta med grafiska element](https://docs.aspose.com/words/net/working-with-graphic-elements/) dokumentationsartikel.

```csharp
public class GradientStopCollection : IEnumerable<GradientStop>
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Count](../../aspose.words.drawing/gradientstopcollection/count/) { get; } | Hämtar ett heltal som anger antalet objekt i samlingen. |
| [Item](../../aspose.words.drawing/gradientstopcollection/item/) { get; set; } | Hämtar eller ställer in en[`GradientStop`](../gradientstop/) objekt i samlingen. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Add](../../aspose.words.drawing/gradientstopcollection/add/)(*[GradientStop](../gradientstop/)*) | Lägger till en specificerad[`GradientStop`](../gradientstop/) till en gradient. |
| [GetEnumerator](../../aspose.words.drawing/gradientstopcollection/getenumerator/)() | Returnerar en uppräknare som itererar genom samlingen. |
| [Insert](../../aspose.words.drawing/gradientstopcollection/insert/)(*int, [GradientStop](../gradientstop/)*) | Infogar en[`GradientStop`](../gradientstop/) till samlingen vid ett angivet index. |
| [Remove](../../aspose.words.drawing/gradientstopcollection/remove/)(*[GradientStop](../gradientstop/)*) | Tar bort en specificerad[`GradientStop`](../gradientstop/) från samlingen. |
| [RemoveAt](../../aspose.words.drawing/gradientstopcollection/removeat/)(*int*) | Tar bort en[`GradientStop`](../gradientstop/) från samlingen vid ett angivet index. |

## Anmärkningar

Du skapar inte instanser av den här klassen direkt. Använd[`GradientStops`](../fill/gradientstops/) egenskap för att komma åt gradientstopp för fyllningsobjekt.

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

* class [GradientStop](../gradientstop/)
* namnutrymme [Aspose.Words.Drawing](../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../)
