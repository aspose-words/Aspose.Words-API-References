---
title: ChartLegend.legendEntries property
linktitle: legendEntries property
articleTitle: legendEntries property
second_title: Aspose.Words for NodeJs
description: "ChartLegend.legendEntries property. Returns a collection of legend entries for all series and trendlines of the parent chart."
type: docs
weight: 30
url: /nodejs-net/aspose.words.drawing.charts/chartlegend/legendEntries/
---

## ChartLegend.legendEntries property

Returns a collection of legend entries for all series and trendlines of the parent chart.


```js
get legendEntries(): Aspose.Words.Drawing.Charts.ChartLegendEntryCollection
```

### Examples

Shows how to work with a legend entry for chart series.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let shape = builder.insertChart(aw.Drawing.Charts.ChartType.Column, 432, 252);

let chart = shape.chart;
let series = chart.series;
series.clear();

let categories = [ "AW Category 1", "AW Category 2" ];

let series1 = series.add("Series 1", categories, [ 1, 2 ]);
series.add("Series 2", categories, [ 3, 4 ]);
series.add("Series 3", categories, [ 5, 6 ]);
series.add("Series 4", categories, [ 0, 0 ]);

let legendEntries = chart.legend.legendEntries;
legendEntries.at(3).isHidden = true;

doc.save(base.artifactsDir + "Charts.legendEntries.docx");
```

### See Also

* module [Aspose.Words.Drawing.Charts](../../)
* class [ChartLegend](../)

