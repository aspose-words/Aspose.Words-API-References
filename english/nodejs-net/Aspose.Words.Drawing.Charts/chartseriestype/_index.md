---
title: ChartSeriesType enumeration
linktitle: ChartSeriesType enumeration
articleTitle: ChartSeriesType enumeration
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Drawing.Charts.ChartSeriesType enumeration. Specifies a type of a chart series."
type: docs
weight: 360
url: /nodejs-net/Aspose.Words.Drawing.Charts/chartseriestype/
---

## ChartSeriesType enumeration

Specifies a type of a chart series.


### Members

| Name | Description |
| --- | --- |
| Area | Represents an Area chart series. |
| AreaStacked | Represents a Stacked Area chart series. |
| AreaPercentStacked | Represents a 100% Stacked Area chart series. |
| Area3D | Represents a 3D Area chart series. |
| Area3DStacked | Represents a 3D Stacked Area chart series. |
| Area3DPercentStacked | Represents a 3D 100% Stacked Area chart series. |
| Bar | Represents a Bar chart series. |
| BarStacked | Represents a Stacked Bar chart series. |
| BarPercentStacked | Represents a 100% Stacked Bar chart series. |
| Bar3D | Represents a 3D Bar chart series. |
| Bar3DStacked | Represents a 3D Stacked Bar chart series. |
| Bar3DPercentStacked | Represents a 3D 100% Stacked Bar chart series. |
| Bubble | Represents a Bubble chart series. |
| Bubble3D | Represents a 3D Bubble chart series. |
| Column | Represents a Column chart series. |
| ColumnStacked | Represents a Stacked Column chart series. |
| ColumnPercentStacked | Represents a 100% Stacked Column chart series. |
| Column3D | Represents a 3D Column chart series. |
| Column3DStacked | Represents a 3D Stacked Column chart series. |
| Column3DPercentStacked | Represents a 3D 100% Stacked Column chart series. |
| Column3DClustered | Represents a 3D Clustered Column chart series. |
| Doughnut | Represents a Doughnut chart series. |
| Line | Represents a Line chart series. |
| LineStacked | Represents a Stacked Line chart series. |
| LinePercentStacked | Represents a 100% Stacked Line chart series. |
| Line3D | Represents a 3D Line chart series. |
| Pie | Represents a Pie chart series. |
| Pie3D | Represents a 3D Pie chart series. |
| PieOfBar | Represents a Pie of Bar chart series. |
| PieOfPie | Represents a Pie of Pie chart series. |
| Radar | Represents a Radar chart series. |
| Scatter | Represents a Scatter chart series. |
| Stock | Represents a Stock chart series. |
| Surface | Represents a Surface chart series. |
| Surface3D | Represents a 3D Surface chart series. |
| Treemap | Represents a Treemap chart series. |
| Sunburst | Represents a Sunburst chart series. |
| Histogram | Represents a Histogram chart series. |
| Pareto | Represents a Pareto chart series. |
| ParetoLine | Represents a Pareto Line chart series. |
| BoxAndWhisker | Represents a Box and Whisker chart series. |
| Waterfall | Represents a Waterfall chart series. |
| Funnel | Represents a Funnel chart series. |
| RegionMap | Represents a Region Map chart series. |

### Examples

Shows how to remove specific chart serie.

```js
let doc = new aw.Document(base.myDir + "Reporting engine template - Chart series.docx");
let chart = doc.getShape(0, true).chart;

// Remove all series of the Column type.
for (var i = chart.series.count - 1; i >= 0; i--)
{
  if (chart.series.at(i).seriesType == aw.Drawing.Charts.ChartSeriesType.Column)
    chart.series.removeAt(i);
}

chart.series.add(
  "Aspose Series",
  [ "Category 1", "Category 2", "Category 3", "Category 4" ],
  [ 5.6, 7.1, 2.9, 8.9 ]);

doc.save(base.artifactsDir + "Charts.RemoveSpecificChartSeries.docx");
```

### See Also

* module [Aspose.Words.Drawing.Charts](../)

