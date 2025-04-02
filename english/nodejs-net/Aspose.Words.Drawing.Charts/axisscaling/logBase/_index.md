---
title: AxisScaling.logBase property
linktitle: logBase property
articleTitle: logBase property
second_title: Aspose.Words for NodeJs
description: "AxisScaling.logBase property. Gets or sets the logarithmic base for a logarithmic axis."
type: docs
weight: 20
url: /nodejs-net/Aspose.Words.Drawing.Charts/axisscaling/logBase/
---

## AxisScaling.logBase property

Gets or sets the logarithmic base for a logarithmic axis.


```js
get logBase(): number
```

### Remarks

The property is not supported by MS Office 2016 new charts.

Valid range of a floating point value is greater than or equal to 2 and less than or 
equal to 1000. The property has effect only if [AxisScaling.type](../type/) is set to 
[AxisScaleType.Logarithmic](../../axisscaletype/#Logarithmic).

Setting this property sets the [AxisScaling.type](../type/) property to [AxisScaleType.Logarithmic](../../axisscaletype/#Logarithmic).





### Examples

Shows how to apply logarithmic scaling to a chart axis.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let chartShape = builder.insertChart(aw.Drawing.Charts.ChartType.Scatter, 450, 300);
let chart = chartShape.chart;

// Clear the chart's demo data series to start with a clean chart.
chart.series.clear();

// Insert a series with X/Y coordinates for five points.
chart.series.add("Series 1",
  [ 1.0, 2.0, 3.0, 4.0, 5.0 ],
  [ 1.0, 20.0, 400.0, 8000.0, 160000.0 ]);

// The scaling of the X-axis is linear by default,
// displaying evenly incrementing values that cover our X-value range (0, 1, 2, 3...).
// A linear axis is not ideal for our Y-values
// since the points with the smaller Y-values will be harder to read.
// A logarithmic scaling with a base of 20 (1, 20, 400, 8000...)
// will spread the plotted points, allowing us to read their values on the chart more easily.
chart.axisY.scaling.type = aw.Drawing.Charts.AxisScaleType.Logarithmic;
chart.axisY.scaling.logBase = 20;

doc.save(base.artifactsDir + "Charts.AxisScaling.docx");
```

### See Also

* module [Aspose.Words.Drawing.Charts](../../)
* class [AxisScaling](../)

