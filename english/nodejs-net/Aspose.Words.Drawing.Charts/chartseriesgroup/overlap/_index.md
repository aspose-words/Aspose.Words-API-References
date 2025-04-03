---
title: ChartSeriesGroup.overlap property
linktitle: overlap property
articleTitle: overlap property
second_title: Aspose.Words for NodeJs
description: "ChartSeriesGroup.overlap property. Gets or sets the percentage of how much the series bars or columns overlap."
type: docs
weight: 80
url: /nodejs-net/aspose.words.drawing.charts/chartseriesgroup/overlap/
---

## ChartSeriesGroup.overlap property

Gets or sets the percentage of how much the series bars or columns overlap.


```js
get overlap(): number
```

### Remarks

Applies to series groups of all bar and column types.

The range of acceptable values is from -100 to 100 inclusive. A value of 0 indicates that there is no
space between bars/columns. If the value is -100, the distance between bars/columns is equal to their width.
A value of 100 means that the bars/columns overlap completely.




### Examples

Show how to configure gap width and overlap.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let shape = builder.insertChart(aw.Drawing.Charts.ChartType.Column, 450, 250);
let seriesGroup = shape.chart.seriesGroups.at(0);

// Set column gap width and overlap.
seriesGroup.gapWidth = 450;
seriesGroup.overlap = -75;

doc.save(base.artifactsDir + "Charts.ConfigureGapOverlap.docx");
```

### See Also

* module [Aspose.Words.Drawing.Charts](../../)
* class [ChartSeriesGroup](../)

