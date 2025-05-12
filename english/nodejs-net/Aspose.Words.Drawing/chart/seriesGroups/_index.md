---
title: Chart.seriesGroups property
linktitle: seriesGroups property
articleTitle: seriesGroups property
second_title: Aspose.Words for Node.js
description: "Chart.seriesGroups property. Provides access to a series group collection of this chart."
type: docs
weight: 90
url: /nodejs-net/aspose.words.drawing/chart/seriesGroups/
---

## Chart.seriesGroups property

Provides access to a series group collection of this chart.


```js
get seriesGroups(): Aspose.Words.Drawing.Charts.ChartSeriesGroupCollection
```

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

* module [Aspose.Words.Drawing](../../)
* class [Chart](../)

