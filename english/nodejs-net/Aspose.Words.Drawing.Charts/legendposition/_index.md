---
title: LegendPosition enumeration
linktitle: LegendPosition enumeration
articleTitle: LegendPosition enumeration
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Drawing.Charts.LegendPosition enumeration. Specifies the possible positions for a chart legend."
type: docs
weight: 480
url: /nodejs-net/aspose.words.drawing.charts/legendposition/
---

## LegendPosition enumeration

Specifies the possible positions for a chart legend.


### Members

| Name | Description |
| --- | --- |
| None | No legend will be shown for the chart. |
| Bottom | Specifies that the legend shall be drawn at the bottom of the chart. |
| Left | Specifies that the legend shall be drawn at the left of the chart. |
| Right | Specifies that the legend shall be drawn at the right of the chart. |
| Top | Specifies that the legend shall be drawn at the top of the chart. |
| TopRight | Specifies that the legend shall be drawn at the top right of the chart. |

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

