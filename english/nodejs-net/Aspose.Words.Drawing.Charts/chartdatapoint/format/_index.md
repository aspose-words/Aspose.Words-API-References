---
title: ChartDataPoint.format property
linktitle: format property
articleTitle: format property
second_title: Aspose.Words for Node.js
description: "ChartDataPoint.format property. Provides access to fill and line formatting of this data point."
type: docs
weight: 30
url: /nodejs-net/aspose.words.drawing.charts/chartdatapoint/format/
---

## ChartDataPoint.format property

Provides access to fill and line formatting of this data point.


```js
get format(): Aspose.Words.Drawing.Charts.ChartFormat
```

### Examples

Shows how to work with data points on a line chart.

```js
test('ChartDataPoint', () => {
  let doc = new aw.Document();
  let builder = new aw.DocumentBuilder(doc);

  let shape = builder.insertChart(aw.Drawing.Charts.ChartType.Line, 500, 350);
  let chart = shape.chart;

  expect(chart.series.count).toEqual(3);
  expect(chart.series.at(0).name).toEqual("Series 1");
  expect(chart.series.at(1).name).toEqual("Series 2");
  expect(chart.series.at(2).name).toEqual("Series 3");

  // Emphasize the chart's data points by making them appear as diamond shapes.
  for (let series of chart.series)
    applyDataPoints(series, 4, aw.Drawing.Charts.MarkerSymbol.Diamond, 15);

  // Smooth out the line that represents the first data series.
  chart.series.at(0).smooth = true;

  // Verify that data points for the first series will not invert their colors if the value is negative.
  for (let p of chart.series.at(0).dataPoints)
  {
    expect(p.invertIfNegative).toEqual(false);
  }

  let dataPoint = chart.series.at(1).dataPoints.at(2);
  dataPoint.format.fill.color = "#FF0000";

  // For a cleaner looking graph, we can clear format individually.
  dataPoint.clearFormat();

  // We can also strip an entire series of data points at once.
  chart.series.at(2).dataPoints.clearFormat();

  doc.save(base.artifactsDir + "Charts.ChartDataPoint.docx");
});
```

Shows how to set individual formatting for categories of a column chart.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let shape = builder.insertChart(aw.Drawing.Charts.ChartType.Column, 432, 252);
let chart = shape.chart;

// Delete default generated series.
chart.series.clear();

// Adding new series.
let series = chart.series.add("Series 1",
  [ "Category 1", "Category 2", "Category 3", "Category 4" ],
  [ 1, 2, 3, 4 ]);

// Set column formatting.
let dataPoints = series.dataPoints;
dataPoints.at(0).format.fill.presetTextured(aw.Drawing.PresetTexture.Denim);
dataPoints.at(1).format.fill.foreColor = "#FF0000";
dataPoints.at(2).format.fill.foreColor = "#FFFF00"
dataPoints.at(3).format.fill.foreColor = "#0000FF";

doc.save(base.artifactsDir + "Charts.DataPointsFormatting.docx");
```

### See Also

* module [Aspose.Words.Drawing.Charts](../../)
* class [ChartDataPoint](../)

