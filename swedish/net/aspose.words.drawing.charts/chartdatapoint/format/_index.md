---
title: ChartDataPoint.Format
linktitle: Format
articleTitle: Format
second_title: Aspose.Words för .NET
description: ChartDataPoint Format fast egendom. Ger tillgång till fyllnings och linjeformatering av denna datapunkt i C#.
type: docs
weight: 30
url: /sv/net/aspose.words.drawing.charts/chartdatapoint/format/
---
## ChartDataPoint.Format property

Ger tillgång till fyllnings- och linjeformatering av denna datapunkt.

```csharp
public ChartFormat Format { get; }
```

## Exempel

Visar hur du ställer in individuell formatering för kategorier i ett kolumndiagram.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;

// Ta bort standardgenererade serier.
chart.Series.Clear();

// Lägger till ny serie.
ChartSeries series = chart.Series.Add("Series 1",
    new[] { "Category 1", "Category 2", "Category 3", "Category 4" },
    new double[] { 1, 2, 3, 4 });

// Ställ in kolumnformatering.
ChartDataPointCollection dataPoints = series.DataPoints;
dataPoints[0].Format.Fill.PresetTextured(PresetTexture.Denim);
dataPoints[1].Format.Fill.ForeColor = Color.Red;
dataPoints[2].Format.Fill.ForeColor = Color.Yellow;
dataPoints[3].Format.Fill.ForeColor = Color.Blue;

doc.Save(ArtifactsDir + "Charts.DataPointsFormatting.docx");
```

### Se även

* class [ChartFormat](../../chartformat/)
* class [ChartDataPoint](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../../)
