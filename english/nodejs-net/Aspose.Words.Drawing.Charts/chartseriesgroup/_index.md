---
title: ChartSeriesGroup class
linktitle: ChartSeriesGroup class
articleTitle: ChartSeriesGroup class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Drawing.Charts.ChartSeriesGroup class. Represents properties of a chart series group, that is, the properties of chart series of the same type associated with the same axes."
type: docs
weight: 340
url: /nodejs-net/aspose.words.drawing.charts/chartseriesgroup/
---

## ChartSeriesGroup class

Represents properties of a chart series group, that is, the properties of chart series of the same type
associated with the same axes.


### Remarks

Combo charts contains multiple chart series groups, with a separate group for each series type.

Also, you can create a chart series group to assign secondary axes to one or more chart series.

To learn more, visit the [
            Working with Charts](https://docs.aspose.com/words/nodejs-net/working-with-charts/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [axisGroup](./axisGroup/) | Gets or sets the axis group to which this series group belongs. |
| [axisX](./axisX/) | Provides access to properties of the X axis of this series group. |
| [axisY](./axisY/) | Provides access to properties of the Y axis of this series group. |
| [bubbleScale](./bubbleScale/) | Gets or sets the size of the bubbles as a percentage of their default size. |
| [doughnutHoleSize](./doughnutHoleSize/) | Gets or sets the hole size of the parent doughnut chart as a percentage. |
| [firstSliceAngle](./firstSliceAngle/) | Gets or sets the angle, in degrees, of the first slice of the parent pie chart. |
| [gapWidth](./gapWidth/) | Gets or sets the percentage of gap width between chart elements. |
| [overlap](./overlap/) | Gets or sets the percentage of how much the series bars or columns overlap. |
| [secondSectionSize](./secondSectionSize/) | Gets or sets the size of the pie chart secondary section as a percentage. |
| [series](./series/) | Gets a collection of series that belong to this series group. |
| [seriesType](./seriesType/) | Gets the type of chart series included in this group. |

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

