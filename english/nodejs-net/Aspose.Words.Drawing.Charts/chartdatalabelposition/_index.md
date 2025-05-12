---
title: ChartDataLabelPosition enumeration
linktitle: ChartDataLabelPosition enumeration
articleTitle: ChartDataLabelPosition enumeration
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Drawing.Charts.ChartDataLabelPosition enumeration. Specifies the position for a chart data label."
type: docs
weight: 210
url: /nodejs-net/aspose.words.drawing.charts/chartdatalabelposition/
---

## ChartDataLabelPosition enumeration

Specifies the position for a chart data label.

Not all series types allow you to specify label positions. And those that do, do not support all values.


### Members

| Name | Description |
| --- | --- |
| Center | Specifies that a data label should be displayed centered on a data marker. |
| Left | Specifies that a data label should be displayed to the left of a data marker. |
| Right | Specifies that a data label should be displayed to the right of a data marker. |
| Above | Specifies that a data label should be displayed above a data marker. |
| Below | Specifies that a data label should be displayed below a data marker. |
| InsideBase | Specifies that a data label should be displayed inside the base of a data marker. |
| InsideEnd | Specifies that a data label should be displayed inside the end of a data marker. |
| OutsideEnd | Specifies that a data label should be displayed outside the end of a data marker. |
| BestFit | Specifies that a data label should be displayed in the most appropriate position. |

### Examples

Shows how to set the position of the data label.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Insert column chart.
let shape = builder.insertChart(aw.Drawing.Charts.ChartType.Column, 432, 252);
let chart = shape.chart;
let seriesColl = chart.series;

// Delete default generated series.
seriesColl.clear();

// Add series.
let series = seriesColl.add(
  "Series 1",
  [ "Category 1", "Category 2", "Category 3" ],
  [ 4, 5, 6 ]);

// Show data labels and set font color.
series.hasDataLabels = true;
let dataLabels = series.dataLabels;
dataLabels.showValue = true;
dataLabels.font.color = "#FFFFFF";

// Set data label position.
dataLabels.position = aw.Drawing.Charts.ChartDataLabelPosition.InsideBase;
dataLabels.at(0).position = aw.Drawing.Charts.ChartDataLabelPosition.OutsideEnd;
dataLabels.at(0).font.color = "#8B0000";

doc.save(base.artifactsDir + "Charts.labelPosition.docx");
```

### See Also

* module [Aspose.Words.Drawing.Charts](../)

