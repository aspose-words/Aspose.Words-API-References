---
title: ChartDataLabelCollection.numberFormat property
linktitle: numberFormat property
articleTitle: numberFormat property
second_title: Aspose.Words for NodeJs
description: "ChartDataLabelCollection.numberFormat property. Gets an [ChartNumberFormat](../../chartnumberformat/) instance allowing to set number format for the data labels of the entire series."
type: docs
weight: 40
url: /nodejs-net/Aspose.Words.Drawing.Charts/chartdatalabelcollection/numberFormat/
---

## ChartDataLabelCollection.numberFormat property

Gets an [ChartNumberFormat](../../chartnumberformat/) instance allowing to set number format for the data labels of the
entire series.



```js
get numberFormat(): Aspose.Words.Drawing.Charts.ChartNumberFormat
```

### Examples

Shows how to enable and configure data labels for a chart series.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Add a line chart, then clear its demo data series to start with a clean chart,
// and then set a title.
let shape = builder.insertChart(aw.Drawing.Charts.ChartType.Line, 500, 300);
let chart = shape.chart;
chart.series.clear();
chart.title.text = "Monthly sales report";

// Insert a custom chart series with months as categories for the X-axis,
// and respective decimal amounts for the Y-axis.
let series = chart.series.add("Revenue",
   [ "January", "February", "March" ],
   [ 25.611, 21.439, 33.750 ]);

// Enable data labels, and then apply a custom number format for values displayed in the data labels.
// This format will treat displayed decimal values as millions of US Dollars.
series.hasDataLabels = true;
let dataLabels = series.dataLabels;
dataLabels.showValue = true;
dataLabels.numberFormat.formatCode = "\"US$\" #,##0.000\"M\"";
dataLabels.font.size = 12;

doc.save(base.artifactsDir + "Charts.DataLabelNumberFormat.docx");
```

### See Also

* module [Aspose.Words.Drawing.Charts](../../)
* class [ChartDataLabelCollection](../)

