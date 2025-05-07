---
title: Chart.dataTable property
linktitle: dataTable property
articleTitle: dataTable property
second_title: Aspose.Words for Node.js
description: "Chart.dataTable property. Provides access to properties of a data table of this chart"
type: docs
weight: 50
url: /nodejs-net/aspose.words.drawing/chart/dataTable/
---

## Chart.dataTable property

Provides access to properties of a data table of this chart.
The data table can be shown using the [ChartDataTable.show](../../../aspose.words.drawing.charts/chartdatatable/show/) property.



```js
get dataTable(): Aspose.Words.Drawing.Charts.ChartDataTable
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

* module [Aspose.Words.Drawing](../../)
* class [Chart](../)

