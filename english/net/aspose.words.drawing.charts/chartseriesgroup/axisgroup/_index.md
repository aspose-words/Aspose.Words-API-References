---
title: ChartSeriesGroup.AxisGroup
linktitle: AxisGroup
articleTitle: AxisGroup
second_title: Aspose.Words for .NET
description: Discover the ChartSeriesGroup AxisGroup property, easily manage your series group’s axis for enhanced data visualization and analysis.
type: docs
weight: 10
url: /net/aspose.words.drawing.charts/chartseriesgroup/axisgroup/
---
## ChartSeriesGroup.AxisGroup property

Gets or sets the axis group to which this series group belongs.

```csharp
public AxisGroup AxisGroup { get; set; }
```

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

Assert.That(newSeriesGroup.SeriesType, Is.EqualTo(ChartSeriesType.Line));

// Add a series to the new series group.
ChartSeries series3 =
    newSeriesGroup.Series.Add("Series of secondary series group", categories, new double[] { 13, 11, 16 });
series3.Format.Stroke.Weight = 3.5;

doc.Save(ArtifactsDir + "Charts.SecondaryAxis.docx");
```

### See Also

* enum [AxisGroup](../../axisgroup/)
* class [ChartSeriesGroup](../)
* namespace [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assembly [Aspose.Words](../../../)
