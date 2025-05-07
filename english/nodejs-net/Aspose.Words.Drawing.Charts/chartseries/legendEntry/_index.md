---
title: ChartSeries.legendEntry property
linktitle: legendEntry property
articleTitle: legendEntry property
second_title: Aspose.Words for Node.js
description: "ChartSeries.legendEntry property. Gets a legend entry for this chart series."
type: docs
weight: 90
url: /nodejs-net/aspose.words.drawing.charts/chartseries/legendEntry/
---

## ChartSeries.legendEntry property

Gets a legend entry for this chart series.


```js
get legendEntry(): Aspose.Words.Drawing.Charts.ChartLegendEntry
```

### Examples

Shows how to work with a legend font.

```js
let doc = new aw.Document(base.myDir + "Reporting engine template - Chart series.docx");
let chart = doc.getShape(0, true).chart;

let chartLegend = chart.legend;
// Set default font size all legend entries.
chartLegend.font.size = 14;
// Change font for specific legend entry.
chartLegend.legendEntries.at(1).font.italic = true;
chartLegend.legendEntries.at(1).font.size = 12;
// Get legend entry for chart series.
let legendEntry = chart.series.at(0).legendEntry;

doc.save(base.artifactsDir + "Charts.LegendFont.docx");
```

### See Also

* module [Aspose.Words.Drawing.Charts](../../)
* class [ChartSeries](../)

