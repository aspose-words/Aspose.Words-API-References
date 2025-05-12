---
title: ChartLegendEntry class
linktitle: ChartLegendEntry class
articleTitle: ChartLegendEntry class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Drawing.Charts.ChartLegendEntry class. Represents a chart legend entry"
type: docs
weight: 270
url: /nodejs-net/aspose.words.drawing.charts/chartlegendentry/
---

## ChartLegendEntry class

Represents a chart legend entry.
To learn more, visit the [Working with Charts](https://docs.aspose.com/words/nodejs-net/working-with-charts/) documentation article.




### Remarks

A legend entry corresponds to a specific chart series or trendline.

The text of the entry is the name of the series or trendline. The text cannot be changed.




### Properties

| Name | Description |
| --- | --- |
| [font](./font/) | Provides access to the font formatting of this legend entry. |
| [isHidden](./isHidden/) | Gets or sets a value indicating whether this entry is hidden in the chart legend. The default value is **false**. |

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

* module [Aspose.Words.Drawing.Charts](../)
* property [ChartSeries.legendEntry](../chartseries/legendEntry/)

