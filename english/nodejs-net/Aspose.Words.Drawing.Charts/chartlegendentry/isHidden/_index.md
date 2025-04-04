---
title: ChartLegendEntry.isHidden property
linktitle: isHidden property
articleTitle: isHidden property
second_title: Aspose.Words for Node.js
description: "ChartLegendEntry.isHidden property. Gets or sets a value indicating whether this entry is hidden in the chart legend"
type: docs
weight: 20
url: /nodejs-net/aspose.words.drawing.charts/chartlegendentry/isHidden/
---

## ChartLegendEntry.isHidden property

Gets or sets a value indicating whether this entry is hidden in the chart legend.
The default value is **false**.



```js
get isHidden(): boolean
```

### Remarks

When a chart legend entry is hidden, it does not affect the corresponding chart series or trendline that
is still displayed on the chart.


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
* class [ChartLegendEntry](../)

