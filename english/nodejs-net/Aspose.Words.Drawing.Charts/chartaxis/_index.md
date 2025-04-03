---
title: ChartAxis class
linktitle: ChartAxis class
articleTitle: ChartAxis class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Drawing.Charts.ChartAxis class. Represents the axis options of the chart"
type: docs
weight: 140
url: /nodejs-net/aspose.words.drawing.charts/chartaxis/
---

## ChartAxis class

Represents the axis options of the chart.
To learn more, visit the [Working with Charts](https://docs.aspose.com/words/nodejs-net/working-with-charts/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [axisBetweenCategories](./axisBetweenCategories/) | Gets or sets a flag indicating whether the value axis crosses the category axis between categories. |
| [baseTimeUnit](./baseTimeUnit/) | Returns or sets the smallest time unit that is represented on the time category axis. |
| [categoryType](./categoryType/) | Gets or sets type of the category axis. |
| [crosses](./crosses/) | Specifies how this axis crosses the perpendicular axis. |
| [crossesAt](./crossesAt/) | Specifies where on the perpendicular axis the axis crosses. |
| [displayUnit](./displayUnit/) | Specifies the scaling value of the display units for the value axis. |
| [document](./document/) | Returns the document containing the parent chart. |
| [format](./format/) | Provides access to line formatting of the axis and fill of the tick labels. |
| [hasMajorGridlines](./hasMajorGridlines/) | Gets or sets a flag indicating whether the axis has major gridlines. |
| [hasMinorGridlines](./hasMinorGridlines/) | Gets or sets a flag indicating whether the axis has minor gridlines. |
| [hidden](./hidden/) | Gets or sets a flag indicating whether this axis is hidden or not. |
| [majorTickMark](./majorTickMark/) | Returns or sets the major tick marks. |
| [majorUnit](./majorUnit/) | Returns or sets the distance between major tick marks. |
| [majorUnitIsAuto](./majorUnitIsAuto/) | Gets or sets a flag indicating whether default distance between major tick marks shall be used. |
| [majorUnitScale](./majorUnitScale/) | Returns or sets the scale value for major tick marks on the time category axis. |
| [minorTickMark](./minorTickMark/) | Returns or sets the minor tick marks for the axis. |
| [minorUnit](./minorUnit/) | Returns or sets the distance between minor tick marks. |
| [minorUnitIsAuto](./minorUnitIsAuto/) | Gets or sets a flag indicating whether default distance between minor tick marks shall be used. |
| [minorUnitScale](./minorUnitScale/) | Returns or sets the scale value for minor tick marks on the time category axis. |
| [numberFormat](./numberFormat/) | Returns a [ChartNumberFormat](../chartnumberformat/) object that allows defining number formats for the axis. |
| [reverseOrder](./reverseOrder/) | Returns or sets a flag indicating whether values of axis should be displayed in reverse order, i.e. from max to min. |
| [scaling](./scaling/) | Provides access to the scaling options of the axis. |
| [tickLabels](./tickLabels/) | Provides access to the properties of the axis tick mark labels. |
| [tickMarkSpacing](./tickMarkSpacing/) | Gets or sets the interval, at which tick marks are drawn. |
| [title](./title/) | Provides access to the axis title properties. |
| [type](./type/) | Returns type of the axis. |

### Examples

Shows how to insert a chart and modify the appearance of its axes.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let shape = builder.insertChart(aw.Drawing.Charts.ChartType.Column, 500, 300);
let chart = shape.chart;

// Clear the chart's demo data series to start with a clean chart.
chart.series.clear();

// Insert a chart series with categories for the X-axis and respective numeric values for the Y-axis.
chart.series.add("Aspose Test Series",
  ["Word", "PDF", "Excel", "GoogleDocs", "Note" ],
  [ 640, 320, 280, 120, 150 ]);

// Chart axes have various options that can change their appearance,
// such as their direction, major/minor unit ticks, and tick marks.
let xAxis = chart.axisX;
xAxis.categoryType = aw.Drawing.Charts.AxisCategoryType.Category;
xAxis.crosses = aw.Drawing.Charts.AxisCrosses.Minimum;
xAxis.reverseOrder = false;
xAxis.majorTickMark = aw.Drawing.Charts.AxisTickMark.Inside;
xAxis.minorTickMark = aw.Drawing.Charts.AxisTickMark.Cross;
xAxis.majorUnit = 10.0;
xAxis.minorUnit = 15.0;
xAxis.tickLabels.offset = 50;
xAxis.tickLabels.position = aw.Drawing.Charts.AxisTickLabelPosition.Low;
xAxis.tickLabels.isAutoSpacing = false;
xAxis.tickMarkSpacing = 1;

let yAxis = chart.axisY;
yAxis.categoryType = aw.Drawing.Charts.AxisCategoryType.Automatic;
yAxis.crosses = aw.Drawing.Charts.AxisCrosses.Maximum;
yAxis.reverseOrder = true;
yAxis.majorTickMark = aw.Drawing.Charts.AxisTickMark.Inside;
yAxis.minorTickMark = aw.Drawing.Charts.AxisTickMark.Cross;
yAxis.majorUnit = 100.0;
yAxis.minorUnit = 20.0;
yAxis.tickLabels.position = aw.Drawing.Charts.AxisTickLabelPosition.NextToAxis;

// Column charts do not have a Z-axis.
expect(chart.axisZ).toBe(null);

doc.save(base.artifactsDir + "Charts.AxisProperties.docx");
```

### See Also

* module [Aspose.Words.Drawing.Charts](../)

