---
title: ChartSeriesCollection class
linktitle: ChartSeriesCollection class
articleTitle: ChartSeriesCollection class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Drawing.Charts.ChartSeriesCollection class. Represents collection of a [ChartSeries](../chartseries/)"
type: docs
weight: 330
url: /nodejs-net/aspose.words.drawing.charts/chartseriescollection/
---

## ChartSeriesCollection class

Represents collection of a [ChartSeries](../chartseries/).
To learn more, visit the [Working with Charts](https://docs.aspose.com/words/nodejs-net/working-with-charts/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [count](./count/) | Returns the number of [ChartSeries](../chartseries/) in this collection. |
| [this[]](./this[]/) |  |

### Methods

| Name | Description |
| --- | --- |
|[ add(seriesName, categories, values)](./add/#string_string[]_number[]) | Adds new [ChartSeries](../chartseries/) to this collection. Use this method to add series to any type of Bar, Column, Line and Surface charts. |
|[ add(seriesName, categories, values, isSubtotal)](./add/#string_string[]_number[]_boolean[]) | Adds new [ChartSeries](../chartseries/) to this collection. Use this method to add series to Waterfall charts. |
|[ add(seriesName, xValues, yValues)](./add/#string_number[]_number[]) | Adds new [ChartSeries](../chartseries/) to this collection. Use this method to add series to any type of Scatter charts. |
|[ add(seriesName, dates, values)](./add/#string_date[]_number[]) | Adds new [ChartSeries](../chartseries/) to this collection. Use this method to add series to any type of Area, Radar and Stock charts. |
|[ add(seriesName, xValues, yValues, bubbleSizes)](./add/#string_number[]_number[]_number[]) | Adds new [ChartSeries](../chartseries/) to this collection. Use this method to add series to any type of Bubble charts. |
|[ add(seriesName, categories, values)](./add/#string_chartmultilevelvalue[]_number[]) | Adds new [ChartSeries](../chartseries/) to this collection. Use this method to add series that have multi-level data categories. |
|[ add(seriesName, xValues)](./add/#string_number[]) | Adds new [ChartSeries](../chartseries/) to this collection. Use this method to add series to Histogram charts. |
|[ clear()](./clear/#default) | Removes all [ChartSeries](../chartseries/) from this collection. |
|[ removeAt(index)](./removeAt/#number) | Removes a [ChartSeries](../chartseries/) at the specified index. |

### Examples

Shows how to add and remove series data in a chart.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Insert a column chart that will contain three series of demo data by default.
let chartShape = builder.insertChart(aw.Drawing.Charts.ChartType.Column, 400, 300);
let chart = chartShape.chart;

// Each series has four decimal values: one for each of the four categories.
// Four clusters of three columns will represent this data.
let chartData = chart.series;

expect(chartData.count).toEqual(3);

// Print the name of every series in the chart.
for (let s of chart.series) {
  console.log(s.name);
}

// These are the names of the categories in the chart.
let categories = [ "Category 1", "Category 2", "Category 3", "Category 4" ];

// We can add a series with new values for existing categories.
// This chart will now contain four clusters of four columns.
chart.series.add("Series 4", categories, [ 4.4, 7.0, 3.5, 2.1 ]);
expect(chartData.count).toEqual(4);
expect(chartData.at(3).name).toEqual("Series 4");

// A chart series can also be removed by index, like this.
// This will remove one of the three demo series that came with the chart.
chartData.removeAt(2);

for (let s in chartData) {
  if (s.name == "Series 3")
    expect(s).toEqual(false);
}
expect(chartData.count).toEqual(3);
expect(chartData.at(2).name).toEqual("Series 4");

// We can also clear all the chart's data at once with this method.
// When creating a new chart, this is the way to wipe all the demo data
// before we can begin working on a blank chart.
chartData.clear();
expect(chartData.count).toEqual(0);
```

### See Also

* module [Aspose.Words.Drawing.Charts](../)

