---
title: ChartSeriesGroup.FirstSliceAngle
linktitle: FirstSliceAngle
articleTitle: FirstSliceAngle
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ChartSeriesGroup FirstSliceAngle för att anpassa cirkeldiagrammets första segmentvinkel i grader för förbättrad datavisualisering.
type: docs
weight: 60
url: /sv/net/aspose.words.drawing.charts/chartseriesgroup/firstsliceangle/
---
## ChartSeriesGroup.FirstSliceAngle property

Hämtar eller ställer in vinkeln, i grader, för den första delen av det överordnade cirkeldiagrammet.

```csharp
public int FirstSliceAngle { get; set; }
```

## Anmärkningar

Gäller seriegrupper avPie ,Pie3D ochDoughnut typer.

Intervallet för acceptabla värden är från 0 till 360. Standardvärdet är 0.

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
