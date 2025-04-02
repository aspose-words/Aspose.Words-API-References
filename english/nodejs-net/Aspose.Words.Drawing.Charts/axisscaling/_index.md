---
title: AxisScaling class
linktitle: AxisScaling class
articleTitle: AxisScaling class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Drawing.Charts.AxisScaling class. Represents the scaling options of the axis"
type: docs
weight: 80
url: /nodejs-net/Aspose.Words.Drawing.Charts/axisscaling/
---

## AxisScaling class

Represents the scaling options of the axis.
To learn more, visit the [Working with Charts](https://docs.aspose.com/words/nodejs-net/working-with-charts/) documentation article.




### Constructors
| Name | Description |
| --- | --- |
| [AxisScaling()](./constructor/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [logBase](./logBase/) | Gets or sets the logarithmic base for a logarithmic axis. |
| [maximum](./maximum/) | Gets or sets the maximum value of the axis. |
| [minimum](./minimum/) | Gets or sets minimum value of the axis. |
| [type](./type/) | Gets or sets scaling type of the axis. |

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

