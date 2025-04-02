---
title: ChartDataTable class
linktitle: ChartDataTable class
articleTitle: ChartDataTable class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Drawing.Charts.ChartDataTable class. Allows to specify properties of a chart data table."
type: docs
weight: 240
url: /nodejs-net/Aspose.Words.Drawing.Charts/chartdatatable/
---

## ChartDataTable class

Allows to specify properties of a chart data table.


### Properties

| Name | Description |
| --- | --- |
| [font](./font/) | Provides access to font formatting of the data table. |
| [format](./format/) | Provides access to fill of text background and border formatting of the data table. |
| [hasHorizontalBorder](./hasHorizontalBorder/) | Gets or sets a flag indicating whether a horizontal border of the data table is displayed. The default value is ``True``. |
| [hasLegendKeys](./hasLegendKeys/) | Gets or sets a flag indicating whether legend keys are displayed in the data table. The default value is ``True``. |
| [hasOutlineBorder](./hasOutlineBorder/) | Gets or sets a flag indicating whether an outline border, that is, a border around series and category names, is displayed. The default value is ``True``. |
| [hasVerticalBorder](./hasVerticalBorder/) | Gets or sets a flag indicating whether a vertical border of the data table is displayed. The default value is ``True``. |
| [show](./show/) | Gets or sets a flag indicating whether the data table will be shown for the chart. Default value is ``False``. |

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

* module [Aspose.Words.Drawing.Charts](../)

