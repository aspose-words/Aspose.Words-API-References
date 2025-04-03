---
title: ChartDataLabelCollection.format property
linktitle: format property
articleTitle: format property
second_title: Aspose.Words for NodeJs
description: "ChartDataLabelCollection.format property. Provides access to fill and line formatting of the data labels."
type: docs
weight: 30
url: /nodejs-net/aspose.words.drawing.charts/chartdatalabelcollection/format/
---

## ChartDataLabelCollection.format property

Provides access to fill and line formatting of the data labels.


```js
get format(): Aspose.Words.Drawing.Charts.ChartFormat
```

### Examples

Shows how to set fill, stroke and callout formatting for chart data labels.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let shape = builder.insertChart(aw.Drawing.Charts.ChartType.Column, 432, 252);
let chart = shape.chart;

// Delete default generated series.
chart.series.clear();

// Add new series.
let series = chart.series.add("AW Series 1",
  [ "AW Category 1", "AW Category 2", "AW Category 3", "AW Category 4" ],
  [ 100, 200, 300, 400 ]);

// Show data labels.
series.hasDataLabels = true;
series.dataLabels.showValue = true;

// Format data labels as callouts.
let format = series.dataLabels.format;
format.shapeType = aw.Drawing.Charts.ChartShapeType.WedgeRectCallout;
format.stroke.color = "#006400";
format.fill.solid("#008000");
series.dataLabels.font.color = "#FFFF00";

// Change fill and stroke of an individual data label.
let labelFormat = series.dataLabels.at(0).format;
labelFormat.stroke.color = "#00008B";
labelFormat.fill.solid("#0000FF");

doc.save(base.artifactsDir + "Charts.FormatDataLables.docx");
```

### See Also

* module [Aspose.Words.Drawing.Charts](../../)
* class [ChartDataLabelCollection](../)

