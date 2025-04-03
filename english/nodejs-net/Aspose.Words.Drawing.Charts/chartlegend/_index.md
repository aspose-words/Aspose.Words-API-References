---
title: ChartLegend class
linktitle: ChartLegend class
articleTitle: ChartLegend class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Drawing.Charts.ChartLegend class. Represents chart legend properties"
type: docs
weight: 260
url: /nodejs-net/Aspose.Words.Drawing.Charts/chartlegend/
---

## ChartLegend class

Represents chart legend properties.
To learn more, visit the [Working with Charts](https://docs.aspose.com/words/nodejs-net/working-with-charts/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [font](./font/) | Provides access to the default font formatting of legend entries. To override the font formatting for a specific legend entry, use the[ChartLegendEntry.font](../chartlegendentry/font/) property. |
| [format](./format/) | Provides access to fill and line formatting of the legend. |
| [legendEntries](./legendEntries/) | Returns a collection of legend entries for all series and trendlines of the parent chart. |
| [overlay](./overlay/) | Determines whether other chart elements shall be allowed to overlap legend. Default value is ``false``. |
| [position](./position/) | Specifies the position of the legend on a chart. |

### Examples

Shows how to edit the appearance of a chart's legend.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let shape = builder.insertChart(aw.Drawing.Charts.ChartType.Line, 450, 300);
let chart = shape.chart;

expect(chart.series.count).toEqual(3);
expect(chart.series.at(0).name).toEqual("Series 1");
expect(chart.series.at(1).name).toEqual("Series 2");
expect(chart.series.at(2).name).toEqual("Series 3");

// Move the chart's legend to the top right corner.
let legend = chart.legend;
legend.position = aw.Drawing.Charts.LegendPosition.TopRight;

// Give other chart elements, such as the graph, more room by allowing them to overlap the legend.
legend.overlay = true;

doc.save(base.artifactsDir + "Charts.ChartLegend.docx");
```

### See Also

* module [Aspose.Words.Drawing.Charts](../)

