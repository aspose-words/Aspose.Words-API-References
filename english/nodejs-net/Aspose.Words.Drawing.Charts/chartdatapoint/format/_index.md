---
title: ChartDataPoint.format property
linktitle: format property
articleTitle: format property
second_title: Aspose.Words for NodeJs
description: "ChartDataPoint.format property. Provides access to fill and line formatting of this data point."
type: docs
weight: 30
url: /nodejs-net/aspose.words.drawing.charts/chartdatapoint/format/
---

## ChartDataPoint.format property

Provides access to fill and line formatting of this data point.


```js
get format(): Aspose.Words.Drawing.Charts.ChartFormat
```

### Examples

Shows how to set individual formatting for categories of a column chart.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let shape = builder.insertChart(aw.Drawing.Charts.ChartType.Column, 432, 252);
let chart = shape.chart;

// Delete default generated series.
chart.series.clear();

// Adding new series.
let series = chart.series.add("Series 1",
  [ "Category 1", "Category 2", "Category 3", "Category 4" ],
  [ 1, 2, 3, 4 ]);

// Set column formatting.
let dataPoints = series.dataPoints;
dataPoints.at(0).format.fill.presetTextured(aw.Drawing.PresetTexture.Denim);
dataPoints.at(1).format.fill.foreColor = "#FF0000";
dataPoints.at(2).format.fill.foreColor = "#FFFF00"
dataPoints.at(3).format.fill.foreColor = "#0000FF";

doc.save(base.artifactsDir + "Charts.DataPointsFormatting.docx");
```

### See Also

* module [Aspose.Words.Drawing.Charts](../../)
* class [ChartDataPoint](../)

