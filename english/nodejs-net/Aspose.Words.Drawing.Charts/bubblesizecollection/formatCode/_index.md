---
title: BubbleSizeCollection.formatCode property
linktitle: formatCode property
articleTitle: formatCode property
second_title: Aspose.Words for Node.js
description: "BubbleSizeCollection.formatCode property. Gets or sets the format code applied to the bubble sizes."
type: docs
weight: 20
url: /nodejs-net/aspose.words.drawing.charts/bubblesizecollection/formatCode/
---

## BubbleSizeCollection.formatCode property

Gets or sets the format code applied to the bubble sizes.


```js
get formatCode(): string
```

### Remarks

Number formatting is used to change the way values appears in the chart.
The examples of number formats:
Number - "#,##0.00"

Currency - "\\"$\\"#,##0.00"

Time - "[$-x-systime]h:mm:ss AM/PM"

Date - "d/mm/yyyy"

Percentage - "0.00%"

Fraction - "# ?/?"

Scientific - "0.00E+00"

Accounting - "_-\\"$\\"\* #,##0.00_-;-\\"$\\"\* #,##0.00_-;_-\\"$\\"\* \\"-\\"??_-;_-@_-"

Custom with color - "[Red]-#,##0.0"




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
* class [BubbleSizeCollection](../)

