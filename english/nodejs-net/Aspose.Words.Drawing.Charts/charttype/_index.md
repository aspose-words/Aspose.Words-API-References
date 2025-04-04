---
title: ChartType enumeration
linktitle: ChartType enumeration
articleTitle: ChartType enumeration
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Drawing.Charts.ChartType enumeration. Specifies type of a chart."
type: docs
weight: 390
url: /nodejs-net/aspose.words.drawing.charts/charttype/
---

## ChartType enumeration

Specifies type of a chart.


### Members

| Name | Description |
| --- | --- |
| Area | Area chart. |
| AreaStacked | Stacked Area chart. |
| AreaPercentStacked | 100% Stacked Area chart. |
| Area3D | 3D Area chart. |
| Area3DStacked | 3D Stacked Area chart. |
| Area3DPercentStacked | 3D 100% Stacked Area chart. |
| Bar | Bar chart. |
| BarStacked | Stacked Bar chart. |
| BarPercentStacked | 100% Stacked Bar chart. |
| Bar3D | 3D Bar chart. |
| Bar3DStacked | 3D Stacked Bar chart. |
| Bar3DPercentStacked | 3D 100% Stacked Bar chart. |
| Bubble | Bubble chart. |
| Bubble3D | 3D Bubble chart. |
| Column | Column chart. |
| ColumnStacked | Stacked Column chart. |
| ColumnPercentStacked | 100% Stacked Column chart. |
| Column3D | 3D Column chart. |
| Column3DStacked | 3D Stacked Column chart. |
| Column3DPercentStacked | 3D 100% Stacked Column chart. |
| Column3DClustered | 3D Clustered Column chart. |
| Doughnut | Doughnut chart. |
| Line | Line chart. |
| LineStacked | Stacked Line chart. |
| LinePercentStacked | 100% Stacked Line chart. |
| Line3D | 3D Line chart. |
| Pie | Pie chart. |
| Pie3D | 3D Pie chart. |
| PieOfBar | Pie of Bar chart. |
| PieOfPie | Pie of Pie chart. |
| Radar | Radar chart. |
| Scatter | Scatter chart. |
| Stock | Stock chart. |
| Surface | Surface chart. |
| Surface3D | 3D Surface chart. |
| Treemap | Treemap chart. |
| Sunburst | Sunburst chart. |
| Histogram | Histogram chart. |
| Pareto | Pareto chart. |
| BoxAndWhisker | Box and Whisker chart. |
| Waterfall | Waterfall chart. |
| Funnel | Funnel chart. |

### Examples

Shows how to create an appropriate type of chart series for a graph type.

```js
test('ChartSeriesCollection', () => {
  let doc = new aw.Document();
  let builder = new aw.DocumentBuilder(doc);

  // There are several ways of populating a chart's series collection.
  // Different series schemas are intended for different chart types.
  // 1 -  Column chart with columns grouped and banded along the X-axis by category:
  let chart = appendChart(builder, aw.Drawing.Charts.ChartType.Column, 500, 300);

  let categories = [ "Category 1", "Category 2", "Category 3" ];

  // Insert two series of decimal values containing a value for each respective category.
  // This column chart will have three groups, each with two columns.
  chart.series.add("Series 1", categories, [ 76.6, 82.1, 91.6 ]);
  chart.series.add("Series 2", categories, [ 64.2, 79.5, 94.0 ]);

  // Categories are distributed along the X-axis, and values are distributed along the Y-axis.
  expect(chart.axisX.type).toEqual(aw.Drawing.Charts.ChartAxisType.Category);
  expect(chart.axisY.type).toEqual(aw.Drawing.Charts.ChartAxisType.Value);

  // 2 -  Area chart with dates distributed along the X-axis:
  chart = appendChart(builder, aw.Drawing.Charts.ChartType.Area, 500, 300);

  let dates = [ Date.parse("2014-03-31"),
    Date.parse("2017-01-23"),
    Date.parse("2017-06-18"),
    Date.parse("2019-11-22"),
    Date.parse("2020-09-07")
  ];

  // Insert a series with a decimal value for each respective date.
  // The dates will be distributed along a linear X-axis,
  // and the values added to this series will create data points.
  chart.series.add("Series 1", dates, [ 15.8, 21.5, 22.9, 28.7, 33.1 ]);

  expect(chart.axisX.type).toEqual(aw.Drawing.Charts.ChartAxisType.Category);
  expect(chart.axisY.type).toEqual(aw.Drawing.Charts.ChartAxisType.Value);

  // 3 -  2D scatter plot:
  chart = appendChart(builder, aw.Drawing.Charts.ChartType.Scatter, 500, 300);

  // Each series will need two decimal arrays of equal length.
  // The first array contains X-values, and the second contains corresponding Y-values
  // of data points on the chart's graph.
  chart.series.add("Series 1",
    [ 3.1, 3.5, 6.3, 4.1, 2.2, 8.3, 1.2, 3.6 ],
    [ 3.1, 6.3, 4.6, 0.9, 8.5, 4.2, 2.3, 9.9 ]);
  chart.series.add("Series 2",
    [ 2.6, 7.3, 4.5, 6.6, 2.1, 9.3, 0.7, 3.3 ],
    [ 7.1, 6.6, 3.5, 7.8, 7.7, 9.5, 1.3, 4.6 ]);

  expect(chart.axisX.type).toEqual(aw.Drawing.Charts.ChartAxisType.Value);
  expect(chart.axisY.type).toEqual(aw.Drawing.Charts.ChartAxisType.Value);

  // 4 -  Bubble chart:
  chart = appendChart(builder, aw.Drawing.Charts.ChartType.Bubble, 500, 300);

  // Each series will need three decimal arrays of equal length.
  // The first array contains X-values, the second contains corresponding Y-values,
  // and the third contains diameters for each of the graph's data points.
  chart.series.add("Series 1",
    [ 1.1, 5.0, 9.8 ],
    [ 1.2, 4.9, 9.9 ],
    [ 2.0, 4.0, 8.0 ]);

  doc.save(base.artifactsDir + "Charts.ChartSeriesCollection.docx");
});
```

### See Also

* module [Aspose.Words.Drawing.Charts](../)

