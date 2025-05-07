---
title: ChartDataTable.format property
linktitle: format property
articleTitle: format property
second_title: Aspose.Words for Node.js
description: "ChartDataTable.format property. Provides access to fill of text background and border formatting of the data table."
type: docs
weight: 20
url: /nodejs-net/aspose.words.drawing.charts/chartdatatable/format/
---

## ChartDataTable.format property

Provides access to fill of text background and border formatting of the data table.


```js
get format(): Aspose.Words.Drawing.Charts.ChartFormat
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

