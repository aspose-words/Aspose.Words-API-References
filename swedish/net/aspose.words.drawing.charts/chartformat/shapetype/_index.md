---
title: ChartFormat.ShapeType
linktitle: ShapeType
articleTitle: ShapeType
second_title: Aspose.Words för .NET
description: Upptäck hur du använder egenskapen ChartFormat ShapeType för att effektivt anpassa dina diagramelement. Förbättra din datavisualisering idag!
type: docs
weight: 30
url: /sv/net/aspose.words.drawing.charts/chartformat/shapetype/
---
## ChartFormat.ShapeType property

Hämtar eller anger formtypen för det överordnade diagramelementet.

```csharp
public ChartShapeType ShapeType { get; set; }
```

## Anmärkningar

För närvarande kan egenskapen endast användas för dataetiketter.

## Exempel

Visar hur man ställer in formatering för fyllning, linje och bildtext för diagramdataetiketter.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;

// Radera standardgenererad serie.
chart.Series.Clear();

// Lägg till ny serie.
ChartSeries series = chart.Series.Add("AW Series 1",
    new string[] { "AW Category 1", "AW Category 2", "AW Category 3", "AW Category 4" },
    new double[] { 100, 200, 300, 400 });

// Visa dataetiketter.
series.HasDataLabels = true;
series.DataLabels.ShowValue = true;

// Formatera dataetiketter som callouts.
ChartFormat format = series.DataLabels.Format;
format.ShapeType = ChartShapeType.WedgeRectCallout;
format.Stroke.Color = Color.DarkGreen;
format.Fill.Solid(Color.Green);
series.DataLabels.Font.Color = Color.Yellow;

// Ändra fyllning och linje för en enskild dataetikett.
ChartFormat labelFormat = series.DataLabels[0].Format;
labelFormat.Stroke.Color = Color.DarkBlue;
labelFormat.Fill.Solid(Color.Blue);

doc.Save(ArtifactsDir + "Charts.FormatDataLables.docx");
```

### Se även

* enum [ChartShapeType](../../chartshapetype/)
* class [ChartFormat](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../../)
