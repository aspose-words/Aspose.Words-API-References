---
title: ChartYValue.fromDouble method
linktitle: fromDouble method
articleTitle: fromDouble method
second_title: Aspose.Words for NodeJs
description: "ChartYValue.fromDouble method. Creates a [ChartYValue](../) instance of the [ChartYValueType.Double](../../chartyvaluetype/#Double) type."
type: docs
weight: 60
url: /nodejs-net/aspose.words.drawing.charts/chartyvalue/fromDouble/
---

## fromDouble(value) {#number}

Creates a [ChartYValue](../) instance of the [ChartYValueType.Double](../../chartyvaluetype/#Double) type.



```js
fromDouble(value: number)
```

| Parameter | Type | Description |
| --- | --- | --- |
| value | number |  |

### Examples

Shows how to populate chart series with data.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder();

let shape = builder.insertChart(aw.Drawing.Charts.ChartType.Column, 432, 252);
let chart = shape.chart;
let series1 = chart.series.at(0);

// Clear X and Y values of the first series.
series1.clearValues();

// Populate the series with data.
series1.add(aw.Drawing.Charts.ChartXValue.fromDouble(3), aw.Drawing.Charts.ChartYValue.fromDouble(10));
series1.add(aw.Drawing.Charts.ChartXValue.fromDouble(5), aw.Drawing.Charts.ChartYValue.fromDouble(5));
series1.add(aw.Drawing.Charts.ChartXValue.fromDouble(7), aw.Drawing.Charts.ChartYValue.fromDouble(11));
series1.add(aw.Drawing.Charts.ChartXValue.fromDouble(9), aw.Drawing.Charts.ChartYValue.fromDouble(17));

let series2 = chart.series.at(1);

// Clear X and Y values of the second series.
series2.clearValues();

// Populate the series with data.
series2.add(aw.Drawing.Charts.ChartXValue.fromDouble(2), aw.Drawing.Charts.ChartYValue.fromDouble(4));
series2.add(aw.Drawing.Charts.ChartXValue.fromDouble(4), aw.Drawing.Charts.ChartYValue.fromDouble(7));
series2.add(aw.Drawing.Charts.ChartXValue.fromDouble(6), aw.Drawing.Charts.ChartYValue.fromDouble(14));
series2.add(aw.Drawing.Charts.ChartXValue.fromDouble(8), aw.Drawing.Charts.ChartYValue.fromDouble(7));

doc.save(base.artifactsDir + "Charts.PopulateChartWithData.docx");
```

### See Also

* module [Aspose.Words.Drawing.Charts](../../)
* class [ChartYValue](../)

