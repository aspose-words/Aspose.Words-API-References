---
title: ChartLegendEntry.font property
linktitle: font property
articleTitle: font property
second_title: Aspose.Words for Node.js
description: "ChartLegendEntry.font property. Provides access to the font formatting of this legend entry."
type: docs
weight: 10
url: /nodejs-net/aspose.words.drawing.charts/chartlegendentry/font/
---

## ChartLegendEntry.font property

Provides access to the font formatting of this legend entry.


```js
get font(): Aspose.Words.Font
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

doc.save(base.artifactsDir + "Charts.LegendFont.docx");
```

### See Also

* module [Aspose.Words.Drawing.Charts](../../)
* class [ChartLegendEntry](../)

