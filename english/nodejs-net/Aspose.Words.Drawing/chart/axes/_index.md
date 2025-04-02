---
title: Chart.axes property
linktitle: axes property
articleTitle: axes property
second_title: Aspose.Words for NodeJs
description: "Chart.axes property. Gets a collection of all axes of this chart."
type: docs
weight: 10
url: /nodejs-net/Aspose.Words.Drawing/chart/axes/
---

## Chart.axes property

Gets a collection of all axes of this chart.


```js
get axes(): Aspose.Words.Drawing.Charts.ChartAxisCollection
```

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

* module [Aspose.Words.Drawing](../../)
* class [Chart](../)

