﻿---
title: ChartSeriesGroupCollection class
linktitle: ChartSeriesGroupCollection class
articleTitle: ChartSeriesGroupCollection class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Drawing.Charts.ChartSeriesGroupCollection class. Represents a collection of [ChartSeriesGroup](../chartseriesgroup/) objects."
type: docs
weight: 350
url: /nodejs-net/aspose.words.drawing.charts/chartseriesgroupcollection/
---

## ChartSeriesGroupCollection class

Represents a collection of [ChartSeriesGroup](../chartseriesgroup/) objects.



### Remarks

To learn more, visit the [Working with Charts](https://docs.aspose.com/words/nodejs-net/working-with-charts/)
documentation article.



### Properties

| Name | Description |
| --- | --- |
| [count](./count/) | Returns the number of series groups in this collection. |
| [this[]](./this[]/) |  |

### Methods

| Name | Description |
| --- | --- |
|[ add(seriesType)](./add/#chartseriestype) | Adds a new series group of the specified series type to this collection. |
|[ removeAt(index)](./removeAt/#number) | Removes a series group at the specified index. All child series will be removed from the chart. |

### Examples

Shows how to work with the secondary axis of chart.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let shape = builder.insertChart(aw.Drawing.Charts.ChartType.Line, 450, 250);
let chart = shape.chart;
let series = chart.series;

// Delete default generated series.
series.clear();

let categories = [ "Category 1", "Category 2", "Category 3" ];
series.add("Series 1 of primary series group", categories, [ 2, 3, 4 ]);
series.add("Series 2 of primary series group", categories, [ 5, 2, 3 ]);

// Create an additional series group, also of the line type.
let newSeriesGroup = chart.seriesGroups.add(aw.Drawing.Charts.ChartSeriesType.Line);
// Specify the use of secondary axes for the new series group.
newSeriesGroup.axisGroup = aw.Drawing.Charts.AxisGroup.Secondary;
// Hide the secondary X axis.
newSeriesGroup.axisX.hidden = true;
// Define title of the secondary Y axis.
newSeriesGroup.axisY.title.show = true;
newSeriesGroup.axisY.title.text = "Secondary Y axis";

expect(newSeriesGroup.seriesType).toEqual(aw.Drawing.Charts.ChartSeriesType.Line);

// Add a series to the new series group.
let series3 =
  newSeriesGroup.series.add("Series of secondary series group", categories, [ 13, 11, 16 ]);
series3.format.stroke.weight = 3.5;

doc.save(base.artifactsDir + "Charts.SecondaryAxis.docx");
```

### See Also

* module [Aspose.Words.Drawing.Charts](../)

