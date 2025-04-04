---
title: ChartSeriesGroupCollection.removeAt method
linktitle: removeAt method
articleTitle: removeAt method
second_title: Aspose.Words for Node.js
description: "ChartSeriesGroupCollection.removeAt method. Removes a series group at the specified index"
type: docs
weight: 40
url: /nodejs-net/aspose.words.drawing.charts/chartseriesgroupcollection/removeAt/
---

## removeAt(index) {#number}

Removes a series group at the specified index. All child series will be removed from the chart.


```js
removeAt(index: number)
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | number |  |

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

