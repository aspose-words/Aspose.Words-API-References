---
title: ChartLegendEntryCollection class
linktitle: ChartLegendEntryCollection class
articleTitle: ChartLegendEntryCollection class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Drawing.Charts.ChartLegendEntryCollection class. Represents a collection of chart legend entries"
type: docs
weight: 280
url: /nodejs-net/Aspose.Words.Drawing.Charts/chartlegendentrycollection/
---

## ChartLegendEntryCollection class

Represents a collection of chart legend entries.
To learn more, visit the [Working with Charts](https://docs.aspose.com/words/nodejs-net/working-with-charts/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [count](./count/) | Returns the number of [ChartLegendEntry](../chartlegendentry/) in this collection. |
| [this[]](./this[]/) |  |

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

* module [Aspose.Words.Drawing.Charts](../)

