---
title: ChartDataTable.show property
linktitle: show property
articleTitle: show property
second_title: Aspose.Words for NodeJs
description: "ChartDataTable.show property. Gets or sets a flag indicating whether the data table will be shown for the chart"
type: docs
weight: 70
url: /nodejs-net/Aspose.Words.Drawing.Charts/chartdatatable/show/
---

## ChartDataTable.show property

Gets or sets a flag indicating whether the data table will be shown for the chart.
Default value is ``false``.



```js
get show(): boolean
```

### Remarks

The following chart types do not support data tables: Scatter, Pie, Doughnut, Surface, Radar, Treemap,
Sunburst, Histogram, Pareto, Box and Whisker, Waterfall, Funnel, Combo charts that include series of
these types. Showing a data table for the chart types throws a System.InvalidOperationException
exception.



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

dataTable.font.italic = true;
dataTable.format.stroke.weight = 1;
dataTable.format.stroke.dashStyle = aw.Drawing.DashStyle.ShortDot;
dataTable.format.stroke.color = "#00008B";

doc.save(base.artifactsDir + "Charts.dataTable.docx");
```

### See Also

* module [Aspose.Words.Drawing.Charts](../../)
* class [ChartDataTable](../)

