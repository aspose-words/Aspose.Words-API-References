---
title: IChartDataPoint.explosion property
linktitle: explosion property
articleTitle: explosion property
second_title: Aspose.Words for NodeJs
description: "IChartDataPoint.explosion property. Specifies the amount the data point shall be moved from the center of the pie"
type: docs
weight: 20
url: /nodejs-net/aspose.words.drawing.charts/ichartdatapoint/explosion/
---

## IChartDataPoint.explosion property

Specifies the amount the data point shall be moved from the center of the pie.
Can be negative, negative means that property is not set and no explosion should be applied.
Applies only to Pie charts.


```js
get explosion(): number
```

### Examples

Shows how to move the slices of a pie chart away from the center.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let shape = builder.insertChart(aw.Drawing.Charts.ChartType.Pie, 500, 350);
let chart = shape.chart;

expect(chart.series.count).toEqual(1);
expect(chart.series.at(0).name).toEqual("Sales");

// "Slices" of a pie chart may be moved away from the center by a distance via the respective data point's Explosion attribute.
// Add a data point to the first portion of the pie chart and move it away from the center by 10 points.
// Aspose.words create data points automatically if them does not exist.
let dataPoint = chart.series.at(0).dataPoints.at(0);
dataPoint.explosion = 10;

// Displace the second portion by a greater distance.
dataPoint = chart.series.at(0).dataPoints.at(1);
dataPoint.explosion = 40;

doc.save(base.artifactsDir + "Charts.PieChartExplosion.docx");
```

### See Also

* module [Aspose.Words.Drawing.Charts](../../)
* class [IChartDataPoint](../)

