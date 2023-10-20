---
title: ChartDataLabelCollection.Format
linktitle: Format
articleTitle: Format
second_title: Aspose.Words för .NET
description: ChartDataLabelCollection Format fast egendom. Ger tillgång till fyllnings och radformatering av dataetiketterna i C#.
type: docs
weight: 30
url: /sv/net/aspose.words.drawing.charts/chartdatalabelcollection/format/
---
## ChartDataLabelCollection.Format property

Ger tillgång till fyllnings- och radformatering av dataetiketterna.

```csharp
public ChartFormat Format { get; }
```

## Exempel

Visar hur du ställer in fyllnings-, linje- och bildtextformatering för diagramdataetiketter.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;

// Ta bort standardgenererade serier.
chart.Series.Clear();

// Lägg till ny serie.
ChartSeries series = chart.Series.Add("AW Series 1",
    new string[] { "AW Category 1", "AW Category 2", "AW Category 3", "AW Category 4" },
    new double[] { 100, 200, 300, 400 });

// Visa dataetiketter.
series.HasDataLabels = true;
series.DataLabels.ShowValue = true;

// Formatera dataetiketter som bildtexter.
ChartFormat format = series.DataLabels.Format;
format.ShapeType = ChartShapeType.WedgeRectCallout;
format.Stroke.Color = Color.DarkGreen;
format.Fill.Solid(Color.Green);
series.DataLabels.Font.Color = Color.Yellow;

// Ändra fyllning och linje för en individuell dataetikett.
ChartFormat labelFormat = series.DataLabels[0].Format;
labelFormat.Stroke.Color = Color.DarkBlue;
labelFormat.Fill.Solid(Color.Blue);

doc.Save(ArtifactsDir + "Charts.FormatDataLables.docx");
```

### Se även

* class [ChartFormat](../../chartformat/)
* class [ChartDataLabelCollection](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../../)
