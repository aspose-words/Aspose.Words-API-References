---
title: ChartLegend.font property
linktitle: font property
articleTitle: font property
second_title: Aspose.Words for NodeJs
description: "ChartLegend.font property. Provides access to the default font formatting of legend entries"
type: docs
weight: 10
url: /nodejs-net/Aspose.Words.Drawing.Charts/chartlegend/font/
---

## ChartLegend.font property

Provides access to the default font formatting of legend entries. To override the font formatting for
a specific legend entry, use the[ChartLegendEntry.font](../../chartlegendentry/font/) property.



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
* class [ChartLegend](../)

