---
title: ChartSeriesCollection.removeAt method
linktitle: removeAt method
articleTitle: removeAt method
second_title: Aspose.Words for NodeJs
description: "ChartSeriesCollection.removeAt method. Removes a [ChartSeries](../../chartseries/) at the specified index."
type: docs
weight: 50
url: /nodejs-net/Aspose.Words.Drawing.Charts/chartseriescollection/removeAt/
---

## removeAt(index) {#number}

Removes a [ChartSeries](../../chartseries/) at the specified index.



```js
removeAt(index: number)
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | number | The zero-based index of the [ChartSeries](../../chartseries/) to remove. |

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

* module [Aspose.Words.Drawing.Charts](../../)
* class [ChartSeriesCollection](../)

