---
title: ChartSeriesGroup.bubbleScale property
linktitle: bubbleScale property
articleTitle: bubbleScale property
second_title: Aspose.Words for NodeJs
description: "ChartSeriesGroup.bubbleScale property. Gets or sets the size of the bubbles as a percentage of their default size."
type: docs
weight: 40
url: /nodejs-net/aspose.words.drawing.charts/chartseriesgroup/bubbleScale/
---

## ChartSeriesGroup.bubbleScale property

Gets or sets the size of the bubbles as a percentage of their default size.


```js
get bubbleScale(): number
```

### Remarks

Applies only to series groups of the [ChartSeriesType.Bubble](../../chartseriestype/#Bubble) and
[ChartSeriesType.Bubble3D](../../chartseriestype/#Bubble3D) types.

The range of acceptable values is from 0 to 300 inclusive. The default value is 100.




### Examples

Show how to set size of the bubbles.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Insert a bubble 3D chart.
let shape = builder.insertChart(aw.Drawing.Charts.ChartType.Bubble3D, 450, 250);
let seriesGroup = shape.chart.seriesGroups.at(0);

// Set bubble scale to 200%.
seriesGroup.bubbleScale = 200;

doc.save(base.artifactsDir + "Charts.bubbleScale.docx");
```

### See Also

* module [Aspose.Words.Drawing.Charts](../../)
* class [ChartSeriesGroup](../)

