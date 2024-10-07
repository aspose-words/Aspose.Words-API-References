---
title: ChartSeriesGroup.DoughnutHoleSize
linktitle: DoughnutHoleSize
articleTitle: DoughnutHoleSize
second_title: Aspose.Words for .NET
description: ChartSeriesGroup DoughnutHoleSize property. Gets or sets the hole size of the parent doughnut chart as a percentage in C#.
type: docs
weight: 50
url: /net/aspose.words.drawing.charts/chartseriesgroup/doughnutholesize/
---
## ChartSeriesGroup.DoughnutHoleSize property

Gets or sets the hole size of the parent doughnut chart as a percentage.

```csharp
public int DoughnutHoleSize { get; set; }
```

## Remarks

Applies only to series groups of the Doughnut type.

The range of acceptable values is from 0 to 90 inclusive. The default value is 75.

## Examples

Shows how to create and format Doughnut chart.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Doughnut, 400, 400);
Chart chart = shape.Chart;
// Delete the default generated series.
chart.Series.Clear();

string[] categories = new string[] { "Category 1", "Category 2", "Category 3" };
chart.Series.Add("Series 1", categories, new double[] { 4, 2, 5 });

// Format the Doughnut chart.
ChartSeriesGroup seriesGroup = chart.SeriesGroups[0];
seriesGroup.DoughnutHoleSize = 10;
seriesGroup.FirstSliceAngle = 270;

doc.Save(ArtifactsDir + "Charts.DoughnutChart.docx");
```

### See Also

* class [ChartSeriesGroup](../)
* namespace [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assembly [Aspose.Words](../../../)
