---
title: ChartDataTable.hasLegendKeys property
linktitle: hasLegendKeys property
articleTitle: hasLegendKeys property
second_title: Aspose.Words for Node.js
description: "ChartDataTable.hasLegendKeys property. Gets or sets a flag indicating whether legend keys are displayed in the data table"
type: docs
weight: 40
url: /nodejs-net/aspose.words.drawing.charts/chartdatatable/hasLegendKeys/
---

## ChartDataTable.hasLegendKeys property

Gets or sets a flag indicating whether legend keys are displayed in the data table.
The default value is ``true``.



```js
get hasLegendKeys(): boolean
```

### Examples

Shows how to show data table with chart series data.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let shape = builder.insertChart(aw.Drawing.Charts.ChartType.Column, 432, 252);
let chart = shape.chart;

let series = chart.series;
series.clear();
let xValues = [ 2020, 2021, 2022, 2023 ];
series.add("Series1", xValues, [ 5, 11, 2, 7 ]);
series.add("Series2", xValues, [ 6, 5.5, 7, 7.8 ]);
series.add("Series3", xValues, [ 10, 8, 7, 9 ]);

let dataTable = chart.dataTable;
dataTable.show = true;

dataTable.hasLegendKeys = false;
dataTable.hasHorizontalBorder = false;
dataTable.hasVerticalBorder = false;
dataTable.hasOutlineBorder = false;

dataTable.font.italic = true;
dataTable.format.stroke.weight = 1;
dataTable.format.stroke.dashStyle = aw.Drawing.DashStyle.ShortDot;
dataTable.format.stroke.color = "#00008B";

doc.save(base.artifactsDir + "Charts.dataTable.docx");
```

### See Also

* module [Aspose.Words.Drawing.Charts](../../)
* class [ChartDataTable](../)

