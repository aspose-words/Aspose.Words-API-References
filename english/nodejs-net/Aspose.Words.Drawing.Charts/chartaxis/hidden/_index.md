---
title: ChartAxis.hidden property
linktitle: hidden property
articleTitle: hidden property
second_title: Aspose.Words for NodeJs
description: "ChartAxis.hidden property. Gets or sets a flag indicating whether this axis is hidden or not."
type: docs
weight: 110
url: /nodejs-net/aspose.words.drawing.charts/chartaxis/hidden/
---

## ChartAxis.hidden property

Gets or sets a flag indicating whether this axis is hidden or not.


```js
get hidden(): boolean
```

### Remarks

Default value is ``false``.



### Examples

Shows how to hide chart axes.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let shape = builder.insertChart(aw.Drawing.Charts.ChartType.Line, 500, 300);
let chart = shape.chart;

// Clear the chart's demo data series to start with a clean chart.
chart.series.clear();

// Add a custom series with categories for the X-axis, and respective decimal values for the Y-axis.
chart.series.add("AW Series 1",
  [ "Item 1", "Item 2", "Item 3", "Item 4", "Item 5" ],
  [ 1.2, 0.3, 2.1, 2.9, 4.2 ]);

// Hide the chart axes to simplify the appearance of the chart. 
chart.axisX.hidden = true;
chart.axisY.hidden = true;

doc.save(base.artifactsDir + "Charts.HideChartAxis.docx");
```

### See Also

* module [Aspose.Words.Drawing.Charts](../../)
* class [ChartAxis](../)

