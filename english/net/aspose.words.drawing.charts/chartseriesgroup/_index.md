---
title: ChartSeriesGroup Class
linktitle: ChartSeriesGroup
articleTitle: ChartSeriesGroup
second_title: Aspose.Words for .NET
description: Aspose.Words.Drawing.Charts.ChartSeriesGroup class. Represents properties of a chart series group that is the properties of chart series of the same type associated with the same axes in C#.
type: docs
weight: 960
url: /net/aspose.words.drawing.charts/chartseriesgroup/
---
## ChartSeriesGroup class

Represents properties of a chart series group, that is, the properties of chart series of the same type associated with the same axes.

```csharp
public class ChartSeriesGroup
```

## Properties

| Name | Description |
| --- | --- |
| [AxisGroup](../../aspose.words.drawing.charts/chartseriesgroup/axisgroup/) { get; set; } | Gets or sets the axis group to which this series group belongs. |
| [AxisX](../../aspose.words.drawing.charts/chartseriesgroup/axisx/) { get; } | Provides access to properties of the X axis of this series group. |
| [AxisY](../../aspose.words.drawing.charts/chartseriesgroup/axisy/) { get; } | Provides access to properties of the Y axis of this series group. |
| [BubbleScale](../../aspose.words.drawing.charts/chartseriesgroup/bubblescale/) { get; set; } | Gets or sets the size of the bubbles as a percentage of their default size. |
| [GapWidth](../../aspose.words.drawing.charts/chartseriesgroup/gapwidth/) { get; set; } | Gets or sets the percentage of gap width between chart elements. |
| [Overlap](../../aspose.words.drawing.charts/chartseriesgroup/overlap/) { get; set; } | Gets or sets the percentage of how much the series bars or columns overlap. |
| [Series](../../aspose.words.drawing.charts/chartseriesgroup/series/) { get; } | Gets a collection of series that belong to this series group. |
| [SeriesType](../../aspose.words.drawing.charts/chartseriesgroup/seriestype/) { get; } | Gets the type of chart series included in this group. |

## Remarks

Combo charts contains multiple chart series groups, with a separate group for each series type.

Also, you can create a chart series group to assign secondary axes to one or more chart series.

To learn more, visit the [ Working with Charts](https://docs.aspose.com/words/net/working-with-charts/) documentation article.

## Examples

Shows how to work with the secondary axis of chart.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 450, 250);
Chart chart = shape.Chart;
ChartSeriesCollection series = chart.Series;

// Delete default generated series.
series.Clear();

string[] categories = new string[] { "Category 1", "Category 2", "Category 3" };
series.Add("Series 1 of primary series group", categories, new double[] { 2, 3, 4 });
series.Add("Series 2 of primary series group", categories, new double[] { 5, 2, 3 });

// Create an additional series group, also of the line type.
ChartSeriesGroup newSeriesGroup = chart.SeriesGroups.Add(ChartSeriesType.Line);
// Specify the use of secondary axes for the new series group.
newSeriesGroup.AxisGroup = AxisGroup.Secondary;
// Hide the secondary X axis.
newSeriesGroup.AxisX.Hidden = true;
// Define title of the secondary Y axis.
newSeriesGroup.AxisY.Title.Show = true;
newSeriesGroup.AxisY.Title.Text = "Secondary Y axis";

// Add a series to the new series group.
ChartSeries series3 =
    newSeriesGroup.Series.Add("Series of secondary series group", categories, new double[] { 13, 11, 16 });
series3.Format.Stroke.Weight = 3.5;

doc.Save(ArtifactsDir + "Charts.SecondaryAxis.docx");
```

### See Also

* namespace [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* assembly [Aspose.Words](../../)
