---
title: ChartSeriesGroup.SecondSectionSize
linktitle: SecondSectionSize
articleTitle: SecondSectionSize
second_title: Aspose.Words for .NET
description: ChartSeriesGroup SecondSectionSize property. Gets or sets the size of the pie chart secondary section as a percentage in C#.
type: docs
weight: 90
url: /net/aspose.words.drawing.charts/chartseriesgroup/secondsectionsize/
---
## ChartSeriesGroup.SecondSectionSize property

Gets or sets the size of the pie chart secondary section as a percentage.

```csharp
public int SecondSectionSize { get; set; }
```

## Remarks

Applies to series groups of the PieOfPie and PieOfBar types.

The range of acceptable values is from 5 to 200 inclusive. The default value is 75.

## Examples

Shows how to create and format pie of Pie chart.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.PieOfPie, 440, 300);
Chart chart = shape.Chart;
// Delete the default generated series.
chart.Series.Clear();

string[] categories = new string[] { "Category 1", "Category 2", "Category 3", "Category 4" };
chart.Series.Add("Series 1", categories, new double[] { 11, 8, 4, 3 });

// Format the Pie of Pie chart.
ChartSeriesGroup seriesGroup = chart.SeriesGroups[0];
seriesGroup.GapWidth = 10;
seriesGroup.SecondSectionSize = 77;

doc.Save(ArtifactsDir + "Charts.PieOfPieChart.docx");
```

### See Also

* class [ChartSeriesGroup](../)
* namespace [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assembly [Aspose.Words](../../../)
