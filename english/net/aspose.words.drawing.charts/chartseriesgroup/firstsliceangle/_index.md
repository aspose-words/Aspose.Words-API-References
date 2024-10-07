---
title: ChartSeriesGroup.FirstSliceAngle
linktitle: FirstSliceAngle
articleTitle: FirstSliceAngle
second_title: Aspose.Words for .NET
description: ChartSeriesGroup FirstSliceAngle property. Gets or sets the angle in degrees of the first slice of the parent pie chart in C#.
type: docs
weight: 60
url: /net/aspose.words.drawing.charts/chartseriesgroup/firstsliceangle/
---
## ChartSeriesGroup.FirstSliceAngle property

Gets or sets the angle, in degrees, of the first slice of the parent pie chart.

```csharp
public int FirstSliceAngle { get; set; }
```

## Remarks

Applies to series groups of the Pie, Pie3D and Doughnut types.

The range of acceptable values is from 0 to 360 inclusive. The default value is 0.

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
