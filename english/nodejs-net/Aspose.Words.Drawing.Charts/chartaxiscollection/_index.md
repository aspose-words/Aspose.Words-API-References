---
title: ChartAxisCollection class
linktitle: ChartAxisCollection class
articleTitle: ChartAxisCollection class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Drawing.Charts.ChartAxisCollection class. Represents a collection of chart axes."
type: docs
weight: 150
url: /nodejs-net/aspose.words.drawing.charts/chartaxiscollection/
---

## ChartAxisCollection class

Represents a collection of chart axes.


### Properties

| Name | Description |
| --- | --- |
| [count](./count/) | Gets the number of axes in this collection. |
| [this[]](./this[]/) |  |

### Examples

Shows how to work with axes collection.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let shape = builder.insertChart(aw.Drawing.Charts.ChartType.Column, 500, 300);
let chart = shape.chart;

// Hide the major grid lines on the primary and secondary Y axes.
for (let axis of chart.axes)
{
  if (axis.type == aw.Drawing.Charts.ChartAxisType.Value)
    axis.hasMajorGridlines = false;
}

doc.save(base.artifactsDir + "Charts.AxisCollection.docx");
```

### See Also

* module [Aspose.Words.Drawing.Charts](../)

