---
title: ChartSeriesGroup.gapWidth property
linktitle: gapWidth property
articleTitle: gapWidth property
second_title: Aspose.Words for NodeJs
description: "ChartSeriesGroup.gapWidth property. Gets or sets the percentage of gap width between chart elements."
type: docs
weight: 70
url: /nodejs-net/aspose.words.drawing.charts/chartseriesgroup/gapWidth/
---

## ChartSeriesGroup.gapWidth property

Gets or sets the percentage of gap width between chart elements.


```js
get gapWidth(): number
```

### Remarks

Applies only to series groups of the bar, column, pie-of-bar, pie-of-pie, histogram, box&whisker,
waterfall and funnel types.

The range of acceptable values is from 0 to 500 inclusive. For bar/column-based series groups, the
property represents the space between bar clusters as a percentage of their width. For pie-of-pie and
bar-of-pie charts, this is the space between the primary and secondary sections of the chart.




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

