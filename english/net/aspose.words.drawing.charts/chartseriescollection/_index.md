---
title: ChartSeriesCollection Class
linktitle: ChartSeriesCollection
articleTitle: ChartSeriesCollection
second_title: Aspose.Words for .NET API Reference
description: Aspose.Words.Drawing.Charts.ChartSeriesCollection class. Represents collection of a ChartSeries in C#.
type: docs
weight: 770
url: /net/aspose.words.drawing.charts/chartseriescollection/
---
## ChartSeriesCollection class

Represents collection of a [`ChartSeries`](../chartseries/).

To learn more, visit the [Working with Charts](https://docs.aspose.com/words/net/working-with-charts/) documentation article.

```csharp
public class ChartSeriesCollection : IEnumerable<ChartSeries>
```

## Properties

| Name | Description |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartseriescollection/count/) { get; } | Returns the number of [`ChartSeries`](../chartseries/) in this collection. |
| [Item](../../aspose.words.drawing.charts/chartseriescollection/item/) { get; } | Returns a [`ChartSeries`](../chartseries/) at the specified index. |

## Methods

| Name | Description |
| --- | --- |
| [Add](../../aspose.words.drawing.charts/chartseriescollection/add/#add_2)(*string, DateTime[], double[]*) | Adds new [`ChartSeries`](../chartseries/) to this collection. Use this method to add series to any type of Area, Radar and Stock charts. |
| [Add](../../aspose.words.drawing.charts/chartseriescollection/add/#add)(*string, double[], double[]*) | Adds new [`ChartSeries`](../chartseries/) to this collection. Use this method to add series to any type of Scatter charts. |
| [Add](../../aspose.words.drawing.charts/chartseriescollection/add/#add_3)(*string, string[], double[]*) | Adds new [`ChartSeries`](../chartseries/) to this collection. Use this method to add series to any type of Bar, Column, Line and Surface charts. |
| [Add](../../aspose.words.drawing.charts/chartseriescollection/add/#add_1)(*string, double[], double[], double[]*) | Adds new [`ChartSeries`](../chartseries/) to this collection. Use this method to add series to any type of Bubble charts. |
| [Clear](../../aspose.words.drawing.charts/chartseriescollection/clear/)() | Removes all [`ChartSeries`](../chartseries/) from this collection. |
| [GetEnumerator](../../aspose.words.drawing.charts/chartseriescollection/getenumerator/)() | Returns an enumerator object. |
| [RemoveAt](../../aspose.words.drawing.charts/chartseriescollection/removeat/)(*int*) | Removes a [`ChartSeries`](../chartseries/) at the specified index. |

## Examples

Shows how to add and remove series data in a chart.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insert a column chart that will contain three series of demo data by default.
Shape chartShape = builder.InsertChart(ChartType.Column, 400, 300);
Chart chart = chartShape.Chart;

// Each series has four decimal values: one for each of the four categories.
// Four clusters of three columns will represent this data.
ChartSeriesCollection chartData = chart.Series;

Assert.AreEqual(3, chartData.Count);

// Print the name of every series in the chart.
using (IEnumerator<ChartSeries> enumerator = chart.Series.GetEnumerator())
{
    while (enumerator.MoveNext())
    {
        Console.WriteLine(enumerator.Current.Name);
    }
}

// These are the names of the categories in the chart.
string[] categories = { "Category 1", "Category 2", "Category 3", "Category 4" };

// We can add a series with new values for existing categories.
// This chart will now contain four clusters of four columns.
chart.Series.Add("Series 4", categories, new[] { 4.4, 7.0, 3.5, 2.1 });
// A chart series can also be removed by index, like this.
// This will remove one of the three demo series that came with the chart.
chartData.RemoveAt(2);

Assert.False(chartData.Any(s => s.Name == "Series 3"));
// We can also clear all the chart's data at once with this method.
// When creating a new chart, this is the way to wipe all the demo data
// before we can begin working on a blank chart.
chartData.Clear();
```

### See Also

* class [ChartSeries](../chartseries/)
* namespace [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* assembly [Aspose.Words](../../)
