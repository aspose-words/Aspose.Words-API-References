---
title: ChartDataPointCollection.clearFormat method
linktitle: clearFormat method
articleTitle: clearFormat method
second_title: Aspose.Words for NodeJs
description: "ChartDataPointCollection.clearFormat method. Clears format of all [ChartDataPoint](../../chartdatapoint/) in this collection."
type: docs
weight: 30
url: /nodejs-net/aspose.words.drawing.charts/chartdatapointcollection/clearFormat/
---

## clearFormat() {#default}

Clears format of all [ChartDataPoint](../../chartdatapoint/) in this collection.



```js
clearFormat()
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

  // For a cleaner looking graph, we can clear format individually.
  chart.series.at(1).dataPoints.at(2).clearFormat();

  // We can also strip an entire series of data points at once.
  chart.series.at(2).dataPoints.clearFormat();

  doc.save(base.artifactsDir + "Charts.ChartDataPoint.docx");
});
```

### See Also

* module [Aspose.Words.Drawing.Charts](../../)
* class [ChartDataPointCollection](../)

