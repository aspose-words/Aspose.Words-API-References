---
title: ChartSeries.bubbleSizes property
linktitle: bubbleSizes property
articleTitle: bubbleSizes property
second_title: Aspose.Words for Node.js
description: "ChartSeries.bubbleSizes property. Gets a collection of bubble sizes for this chart series."
type: docs
weight: 20
url: /nodejs-net/aspose.words.drawing.charts/chartseries/bubbleSizes/
---

## ChartSeries.bubbleSizes property

Gets a collection of bubble sizes for this chart series.


```js
get bubbleSizes(): Aspose.Words.Drawing.Charts.BubbleSizeCollection
```

### Examples

Shows how to work with the format code of the chart data.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Insert a Bubble chart.
let shape = builder.insertChart(aw.Drawing.Charts.ChartType.Bubble, 432, 252);
let chart = shape.chart;

// Delete default generated series.
chart.series.clear();

let series = chart.series.add(
  "Series1",
  [ 1, 1.9, 2.45, 3 ],
  [ 1, -0.9, 1.82, 0 ],
  [ 2, 1.1, 2.95, 2 ]);

// Show data labels.
series.hasDataLabels = true;
series.dataLabels.showCategoryName = true;
series.dataLabels.showValue = true;
series.dataLabels.showBubbleSize = true;

// Set data format codes.
series.xvalues.formatCode = "#,##0.0#";
series.yvalues.formatCode = "#,##0.0#;[Red]\\-#,##0.0#";
series.bubbleSizes.formatCode = "#,##0.0#";

doc.save(base.artifactsDir + "Charts.formatCode.docx");
```

### See Also

* module [Aspose.Words.Drawing.Charts](../../)
* class [ChartSeries](../)

