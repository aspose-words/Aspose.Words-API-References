---
title: ChartAxis.CrossesAt
linktitle: CrossesAt
articleTitle: CrossesAt
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ChartAxis CrossesAt för att enkelt definiera skärningspunkter på diagrammets vinkelräta axel för förbättrad datavisualisering.
type: docs
weight: 50
url: /sv/net/aspose.words.drawing.charts/chartaxis/crossesat/
---
## ChartAxis.CrossesAt property

Anger var axeln skärs på den vinkelräta axeln.

```csharp
public double CrossesAt { get; set; }
```

## Anmärkningar

Fastigheten har endast verkan om[`Crosses`](../crosses/) är inställda påCustom. Det stöds inte av de nya diagrammen i MS Office 2016.

Enheterna bestäms av axeltypen. När axeln är en värdeaxel är värdet för egenskapen ett decimaltal på värdeaxeln. När axeln är en tidskategoriaxel definieras värdet som , ett heltal dagar i förhållande till basdatumet (30/12/1899). För en textkategoriaxel är värdet , ett heltal kategorinummer, som börjar med 1 som den första kategorin.

## Exempel

Visar hur man får en grafaxel att korsa vid en anpassad plats.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 450, 250);
Chart chart = shape.Chart;

Assert.AreEqual(3, chart.Series.Count);
Assert.AreEqual("Series 1", chart.Series[0].Name);
Assert.AreEqual("Series 2", chart.Series[1].Name);
Assert.AreEqual("Series 3", chart.Series[2].Name);

// För stapeldiagram korsar Y-axeln vid noll som standard,
// vilket innebär att kolumner för alla värden under noll pekar nedåt för att representera negativa värden.
// Vi kan ställa in ett annat värde för Y-axelns korsning. I det här fallet ställer vi in det till 3.
ChartAxis axis = chart.AxisX;
axis.Crosses = AxisCrosses.Custom;
axis.CrossesAt = 3;
axis.AxisBetweenCategories = true;

doc.Save(ArtifactsDir + "Charts.AxisCross.docx");
```

### Se även

* class [ChartAxis](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../../)
