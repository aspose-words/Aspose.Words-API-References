﻿---
title: AxisTickLabels class
linktitle: AxisTickLabels class
articleTitle: AxisTickLabels class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Drawing.Charts.AxisTickLabels class. Represents properties of axis tick mark labels."
type: docs
weight: 100
url: /nodejs-net/aspose.words.drawing.charts/axisticklabels/
---

## AxisTickLabels class

Represents properties of axis tick mark labels.


### Properties

| Name | Description |
| --- | --- |
| [alignment](./alignment/) | Gets or sets text alignment of the axis tick labels. |
| [font](./font/) | Provides access to font formatting of the tick labels. |
| [isAutoSpacing](./isAutoSpacing/) | Gets or sets a flag indicating whether to use automatic interval for drawing the tick labels. |
| [offset](./offset/) | Gets or sets the distance of the tick labels from the axis. |
| [orientation](./orientation/) | Gets or sets the orientation of the tick label text. |
| [position](./position/) | Gets or sets the position of the tick labels on the axis. |
| [rotation](./rotation/) | Gets or sets the rotation of the tick labels in degrees. |
| [spacing](./spacing/) | Gets or sets the interval at which the tick labels are drawn. |

### Examples

Shows how to insert a chart and modify the appearance of its axes.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let shape = builder.insertChart(aw.Drawing.Charts.ChartType.Column, 500, 300);
let chart = shape.chart;

// Clear the chart's demo data series to start with a clean chart.
chart.series.clear();

// Insert a chart series with categories for the X-axis and respective numeric values for the Y-axis.
chart.series.add("Aspose Test Series",
  ["Word", "PDF", "Excel", "GoogleDocs", "Note" ],
  [ 640, 320, 280, 120, 150 ]);

// Chart axes have various options that can change their appearance,
// such as their direction, major/minor unit ticks, and tick marks.
let xAxis = chart.axisX;
xAxis.categoryType = aw.Drawing.Charts.AxisCategoryType.Category;
xAxis.crosses = aw.Drawing.Charts.AxisCrosses.Minimum;
xAxis.reverseOrder = false;
xAxis.majorTickMark = aw.Drawing.Charts.AxisTickMark.Inside;
xAxis.minorTickMark = aw.Drawing.Charts.AxisTickMark.Cross;
xAxis.majorUnit = 10.0;
xAxis.minorUnit = 15.0;
xAxis.tickLabels.offset = 50;
xAxis.tickLabels.position = aw.Drawing.Charts.AxisTickLabelPosition.Low;
xAxis.tickLabels.isAutoSpacing = false;
xAxis.tickMarkSpacing = 1;

expect(xAxis.document.referenceEquals(doc)).toEqual(true);

let yAxis = chart.axisY;
yAxis.categoryType = aw.Drawing.Charts.AxisCategoryType.Automatic;
yAxis.crosses = aw.Drawing.Charts.AxisCrosses.Maximum;
yAxis.reverseOrder = true;
yAxis.majorTickMark = aw.Drawing.Charts.AxisTickMark.Inside;
yAxis.minorTickMark = aw.Drawing.Charts.AxisTickMark.Cross;
yAxis.majorUnit = 100.0;
yAxis.minorUnit = 20.0;
yAxis.tickLabels.position = aw.Drawing.Charts.AxisTickLabelPosition.NextToAxis;
yAxis.tickLabels.alignment = aw.ParagraphAlignment.Center;
yAxis.tickLabels.font.color = "#FF0000";
yAxis.tickLabels.spacing = 1;

// Column charts do not have a Z-axis.
expect(chart.axisZ).toBe(null);

doc.save(base.artifactsDir + "Charts.AxisProperties.docx");
```

### See Also

* module [Aspose.Words.Drawing.Charts](../)

