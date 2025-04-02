---
title: ChartAxis.numberFormat property
linktitle: numberFormat property
articleTitle: numberFormat property
second_title: Aspose.Words for NodeJs
description: "ChartAxis.numberFormat property. Returns a [ChartNumberFormat](../../chartnumberformat/) object that allows defining number formats for the axis."
type: docs
weight: 200
url: /nodejs-net/Aspose.Words.Drawing.Charts/chartaxis/numberFormat/
---

## ChartAxis.numberFormat property

Returns a [ChartNumberFormat](../../chartnumberformat/) object that allows defining number formats for the axis.



```js
get numberFormat(): Aspose.Words.Drawing.Charts.ChartNumberFormat
```

### Examples

Shows how to set formatting for chart values.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let shape = builder.insertChart(aw.Drawing.Charts.ChartType.Column, 500, 300);
let chart = shape.chart;

// Clear the chart's demo data series to start with a clean chart.
chart.series.clear();

// Add a custom series to the chart with categories for the X-axis,
// and large respective numeric values for the Y-axis. 
chart.series.add("Aspose Test Series",
  [ "Word", "PDF", "Excel", "GoogleDocs", "Note" ],
  [ 1900000, 850000, 2100000, 600000, 1500000 ]);

// Set the number format of the Y-axis tick labels to not group digits with commas. 
chart.axisY.numberFormat.formatCode = "#,##0";

// This flag can override the above value and draw the number format from the source cell.
expect(chart.axisY.numberFormat.isLinkedToSource).toEqual(false);

doc.save(base.artifactsDir + "Charts.SetNumberFormatToChartAxis.docx");
```

### See Also

* module [Aspose.Words.Drawing.Charts](../../)
* class [ChartAxis](../)

