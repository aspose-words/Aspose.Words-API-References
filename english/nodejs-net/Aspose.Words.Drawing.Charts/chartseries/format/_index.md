---
title: ChartSeries.format property
linktitle: format property
articleTitle: format property
second_title: Aspose.Words for NodeJs
description: "ChartSeries.format property. Provides access to fill and line formatting of the series."
type: docs
weight: 60
url: /nodejs-net/aspose.words.drawing.charts/chartseries/format/
---

## ChartSeries.format property

Provides access to fill and line formatting of the series.


```js
get format(): Aspose.Words.Drawing.Charts.ChartFormat
```

### Examples

Sows how to set series color.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let shape = builder.insertChart(aw.Drawing.Charts.ChartType.Column, 432, 252);

let chart = shape.chart;
let seriesColl = chart.series;

// Delete default generated series.
seriesColl.clear();

// Create category names array.
let categories = [ "Category 1", "Category 2" ];

// Adding new series. Value and category arrays must be the same size.
let series1 = seriesColl.add("Series 1", categories, [ 1, 2 ]);
let series2 = seriesColl.add("Series 2", categories, [ 3, 4 ]);
let series3 = seriesColl.add("Series 3", categories, [ 5, 6 ]);

// Set series color.
series1.format.fill.foreColor = "#FF0000";
series2.format.fill.foreColor = "#FFFF00";
series3.format.fill.foreColor = "#0000FF";

doc.save(base.artifactsDir + "Charts.SeriesColor.docx");
```

### See Also

* module [Aspose.Words.Drawing.Charts](../../)
* class [ChartSeries](../)

