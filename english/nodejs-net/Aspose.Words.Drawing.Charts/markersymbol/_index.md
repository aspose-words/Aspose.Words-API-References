---
title: MarkerSymbol enumeration
linktitle: MarkerSymbol enumeration
articleTitle: MarkerSymbol enumeration
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Drawing.Charts.MarkerSymbol enumeration. Specifies marker symbol style."
type: docs
weight: 490
url: /nodejs-net/aspose.words.drawing.charts/markersymbol/
---

## MarkerSymbol enumeration

Specifies marker symbol style.


### Members

| Name | Description |
| --- | --- |
| Default | Specifies a default marker symbol shall be drawn at each data point. |
| Circle | Specifies a circle shall be drawn at each data point. |
| Dash | Specifies a dash shall be drawn at each data point. |
| Diamond | Specifies a diamond shall be drawn at each data point. |
| Dot | Specifies a dot shall be drawn at each data point. |
| None | Specifies nothing shall be drawn at each data point. |
| Picture | Specifies a picture shall be drawn at each data point. |
| Plus | Specifies a plus shall be drawn at each data point. |
| Square | Specifies a square shall be drawn at each data point. |
| Star | Specifies a star shall be drawn at each data point. |
| Triangle | Specifies a triangle shall be drawn at each data point. |
| X | Specifies an X shall be drawn at each data point. |

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

### See Also

* module [Aspose.Words.Drawing.Charts](../)

