---
title: ChartSeriesGroupCollection.count property
linktitle: count property
articleTitle: count property
second_title: Aspose.Words for Node.js
description: "ChartSeriesGroupCollection.count property. Returns the number of series groups in this collection."
type: docs
weight: 10
url: /nodejs-net/aspose.words.drawing.charts/chartseriesgroupcollection/count/
---

## ChartSeriesGroupCollection.count property

Returns the number of series groups in this collection.


```js
get count(): number
```

### Examples

Show how to remove secondary axis.

```js
let doc = new aw.Document(base.myDir + "Combo chart.docx");

let shape = doc.getShape(0, true);
let chart = shape.chart;
let seriesGroups = chart.seriesGroups;

// Find secondary axis and remove from the collection.
for (let i = 0; i < seriesGroups.count; i++)
  if (seriesGroups.at(i).axisGroup == aw.Drawing.Charts.AxisGroup.Secondary)
    seriesGroups.removeAt(i);
```

### See Also

* module [Aspose.Words.Drawing.Charts](../../)
* class [ChartSeriesGroupCollection](../)

