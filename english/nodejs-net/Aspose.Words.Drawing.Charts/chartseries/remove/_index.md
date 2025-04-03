---
title: ChartSeries.remove method
linktitle: remove method
articleTitle: remove method
second_title: Aspose.Words for NodeJs
description: "ChartSeries.remove method. Removes the X value, Y value, and bubble size, if supported, from the chart series at the specified index"
type: docs
weight: 210
url: /nodejs-net/aspose.words.drawing.charts/chartseries/remove/
---

## remove(index) {#number}

Removes the X value, Y value, and bubble size, if supported, from the chart series at the specified index.
The corresponding data point and data label are also removed.


```js
remove(index: number)
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | number |  |

### Examples

Shows how to add/remove chart data values.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder();

let shape = builder.insertChart(aw.Drawing.Charts.ChartType.Column, 432, 252);
let chart = shape.chart;
let department1Series = chart.series.at(0);
let department2Series = chart.series.at(1);

// Remove the first value in the both series.
department1Series.remove(0);
department2Series.remove(0);

// Add new values to the both series.
let newXCategory = aw.Drawing.Charts.ChartXValue.fromString("Q1, 2023");
department1Series.add(newXCategory, aw.Drawing.Charts.ChartYValue.fromDouble(10.3));
department2Series.add(newXCategory, aw.Drawing.Charts.ChartYValue.fromDouble(5.7));

doc.save(base.artifactsDir + "Charts.ChartDataValues.docx");
```

### See Also

* module [Aspose.Words.Drawing.Charts](../../)
* class [ChartSeries](../)

