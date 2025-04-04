---
title: ChartNumberFormat.formatCode property
linktitle: formatCode property
articleTitle: formatCode property
second_title: Aspose.Words for Node.js
description: "ChartNumberFormat.formatCode property. Gets or sets the format code applied to a data label."
type: docs
weight: 10
url: /nodejs-net/aspose.words.drawing.charts/chartnumberformat/formatCode/
---

## ChartNumberFormat.formatCode property

Gets or sets the format code applied to a data label.


```js
get formatCode(): string
```

### Remarks

Number formatting is used to change the way a value appears in data label and can be used in some very creative ways.
The examples of number formats:
Number - "#,##0.00"

Currency - "\\"$\\"#,##0.00"

Time - "[$-x-systime]h:mm:ss AM/PM"

Date - "d/mm/yyyy"

Percentage - "0.00%"

Fraction - "# ?/?"

Scientific - "0.00E+00"

Text - "@"

Accounting - "_-\\"$\\"\* #,##0.00_-;-\\"$\\"\* #,##0.00_-;_-\\"$\\"\* \\"-\\"??_-;_-@_-"

Custom with color - "[Red]-#,##0.0"




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
* class [ChartNumberFormat](../)

