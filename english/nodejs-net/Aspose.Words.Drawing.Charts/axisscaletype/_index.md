---
title: AxisScaleType enumeration
linktitle: AxisScaleType enumeration
articleTitle: AxisScaleType enumeration
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Drawing.Charts.AxisScaleType enumeration. Specifies the possible scale types for an axis."
type: docs
weight: 70
url: /nodejs-net/aspose.words.drawing.charts/axisscaletype/
---

## AxisScaleType enumeration

Specifies the possible scale types for an axis.


### Members

| Name | Description |
| --- | --- |
| Linear | Linear scaling. |
| Logarithmic | Logarithmic scaling. |

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

* module [Aspose.Words.Drawing.Charts](../)

