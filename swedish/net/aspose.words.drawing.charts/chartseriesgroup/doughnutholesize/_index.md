---
title: ChartSeriesGroup.DoughnutHoleSize
linktitle: DoughnutHoleSize
articleTitle: DoughnutHoleSize
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ChartSeriesGroup DoughnutHoleSize för att enkelt anpassa hålstorleken i procent i ditt ringdiagram för förbättrad datavisualisering.
type: docs
weight: 50
url: /sv/net/aspose.words.drawing.charts/chartseriesgroup/doughnutholesize/
---
## ChartSeriesGroup.DoughnutHoleSize property

Hämtar eller ställer in hålstorleken i det överordnade ringdiagrammet som en procentandel.

```csharp
public int DoughnutHoleSize { get; set; }
```

## Anmärkningar

Gäller endast seriegrupper avDoughnut typ.

Intervallet för acceptabla värden är från 0 till 90. Standardvärdet är 75.

## Exempel

Visar hur man skapar och formaterar ett ringdiagram.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Doughnut, 400, 400);
Chart chart = shape.Chart;
// Radera den standardgenererade serien.
chart.Series.Clear();

string[] categories = new string[] { "Category 1", "Category 2", "Category 3" };
chart.Series.Add("Series 1", categories, new double[] { 4, 2, 5 });

// Formatera ringdiagrammet.
ChartSeriesGroup seriesGroup = chart.SeriesGroups[0];
seriesGroup.DoughnutHoleSize = 10;
seriesGroup.FirstSliceAngle = 270;

doc.Save(ArtifactsDir + "Charts.DoughnutChart.docx");
```

### Se även

* class [ChartSeriesGroup](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../../)
