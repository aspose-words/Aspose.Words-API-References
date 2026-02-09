---
title: ChartSeriesGroupCollection Class
linktitle: ChartSeriesGroupCollection
articleTitle: ChartSeriesGroupCollection
second_title: Aspose.Words for .NET
description: Explore the Aspose.Words.ChartSeriesGroupCollection class, your go-to solution for managing and organizing ChartSeriesGroup objects effortlessly.
type: docs
weight: 1100
url: /net/aspose.words.drawing.charts/chartseriesgroupcollection/
---
## ChartSeriesGroupCollection class

Represents a collection of [`ChartSeriesGroup`](../chartseriesgroup/) objects.

```csharp
public class ChartSeriesGroupCollection : IEnumerable<ChartSeriesGroup>
```

## Properties

| Name | Description |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartseriesgroupcollection/count/) { get; } | Returns the number of series groups in this collection. |
| [Item](../../aspose.words.drawing.charts/chartseriesgroupcollection/item/) { get; } | Returns a [`ChartSeriesGroup`](../chartseriesgroup/) at the specified index. |

## Methods

| Name | Description |
| --- | --- |
| [Add](../../aspose.words.drawing.charts/chartseriesgroupcollection/add/)(*[ChartSeriesType](../chartseriestype/)*) | Adds a new series group of the specified series type to this collection. |
| [GetEnumerator](../../aspose.words.drawing.charts/chartseriesgroupcollection/getenumerator/)() | Returns an enumerator object. |
| [RemoveAt](../../aspose.words.drawing.charts/chartseriesgroupcollection/removeat/)(*int*) | Removes a series group at the specified index. All child series will be removed from the chart. |

## Remarks

To learn more, visit the [Working with Charts](https://docs.aspose.com/words/net/working-with-charts/) documentation article.

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

* class [ChartSeriesGroup](../chartseriesgroup/)
* namespace [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* assembly [Aspose.Words](../../)
