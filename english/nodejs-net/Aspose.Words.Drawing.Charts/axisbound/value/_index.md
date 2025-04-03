---
title: AxisBound.value property
linktitle: value property
articleTitle: value property
second_title: Aspose.Words for NodeJs
description: "AxisBound.value property. Returns numeric value of axis bound."
type: docs
weight: 30
url: /nodejs-net/aspose.words.drawing.charts/axisbound/value/
---

## AxisBound.value property

Returns numeric value of axis bound.


```js
get value(): number
```

### Examples

Shows how to set custom axis bounds.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let chartShape = builder.insertChart(aw.Drawing.Charts.ChartType.Scatter, 450, 300);
let chart = chartShape.chart;

// Clear the chart's demo data series to start with a clean chart.
chart.series.clear();

// Add a series with two decimal arrays. The first array contains the X-values,
// and the second contains corresponding Y-values for points in the scatter chart.
chart.series.add("Series 1",
  [ 1.1, 5.4, 7.9, 3.5, 2.1, 9.7 ],
  [ 2.1, 0.3, 0.6, 3.3, 1.4, 1.9 ]);

// By default, default scaling is applied to the graph's X and Y-axes,
// so that both their ranges are big enough to encompass every X and Y-value of every series.
expect(chart.axisX.scaling.minimum.isAuto).toEqual(true);

// We can define our own axis bounds.
// In this case, we will make both the X and Y-axis rulers show a range of 0 to 10.
chart.axisX.scaling.minimum = new aw.Drawing.Charts.AxisBound(0);
chart.axisX.scaling.maximum = new aw.Drawing.Charts.AxisBound(10);
chart.axisY.scaling.minimum = new aw.Drawing.Charts.AxisBound(0);
chart.axisY.scaling.maximum = new aw.Drawing.Charts.AxisBound(10);

expect(chart.axisX.scaling.minimum.isAuto).toEqual(false);
expect(chart.axisY.scaling.minimum.isAuto).toEqual(false);

// Create a line chart with a series requiring a range of dates on the X-axis, and decimal values for the Y-axis.
chartShape = builder.insertChart(aw.Drawing.Charts.ChartType.Line, 450, 300);
chart = chartShape.chart;
chart.series.clear();

let dates = [ Date.parse("1973-05-11"),
  Date.parse("1981-02-04"),
  Date.parse("1985-09-23"),
  Date.parse("1989-06-28"),
  Date.parse("1994-12-15")
];

chart.series.add("Series 1", dates, [ 3.0, 4.7, 5.9, 7.1, 8.9 ]);

// We can set axis bounds in the form of dates as well, limiting the chart to a period.
// Setting the range to 1980-1990 will omit the two of the series values
// that are outside of the range from the graph.
chart.axisX.scaling.minimum = new aw.Drawing.Charts.AxisBound(Date.parse("1980-01-01"));
chart.axisX.scaling.maximum = new aw.Drawing.Charts.AxisBound(Date.parse("1990-01-01"));

doc.save(base.artifactsDir + "Charts.AxisBound.docx");
```

### See Also

* module [Aspose.Words.Drawing.Charts](../../)
* class [AxisBound](../)

