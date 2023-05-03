---
title: ChartSeriesCollection.Clear
linktitle: Clear
articleTitle: Clear
second_title: Aspose.Words for .NET API Reference
description: ChartSeriesCollection Clear method. Removes all ChartSeries from this collection in C#.
type: docs
weight: 40
url: /net/aspose.words.drawing.charts/chartseriescollection/clear/
---
## ChartSeriesCollection.Clear method

Removes all [`ChartSeries`](../../chartseries/) from this collection.

```csharp
public void Clear()
```

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

* class [ChartSeriesCollection](../)
* namespace [Aspose.Words.Drawing.Charts](../../chartseriescollection/)
* assembly [Aspose.Words](../../../)
