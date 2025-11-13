---
title: ChartSeriesType enumeration
linktitle: ChartSeriesType enumeration
articleTitle: ChartSeriesType enumeration
second_title: Aspose.Words for Python
description: "aspose.words.drawing.charts.ChartSeriesType enumeration. Specifies a type of a chart series."
type: docs
weight: 370
url: /python-net/aspose.words.drawing.charts/chartseriestype/
---

## ChartSeriesType enumeration

Specifies a type of a chart series.


### Members

| Name | Description |
| --- | --- |
| AREA | Represents an Area chart series. |
| AREA_STACKED | Represents a Stacked Area chart series. |
| AREA_PERCENT_STACKED | Represents a 100% Stacked Area chart series. |
| AREA_3D | Represents a 3D Area chart series. |
| AREA_3D_STACKED | Represents a 3D Stacked Area chart series. |
| AREA_3D_PERCENT_STACKED | Represents a 3D 100% Stacked Area chart series. |
| BAR | Represents a Bar chart series. |
| BAR_STACKED | Represents a Stacked Bar chart series. |
| BAR_PERCENT_STACKED | Represents a 100% Stacked Bar chart series. |
| BAR_3D | Represents a 3D Bar chart series. |
| BAR_3D_STACKED | Represents a 3D Stacked Bar chart series. |
| BAR_3D_PERCENT_STACKED | Represents a 3D 100% Stacked Bar chart series. |
| BUBBLE | Represents a Bubble chart series. |
| BUBBLE_3D | Represents a 3D Bubble chart series. |
| COLUMN | Represents a Column chart series. |
| COLUMN_STACKED | Represents a Stacked Column chart series. |
| COLUMN_PERCENT_STACKED | Represents a 100% Stacked Column chart series. |
| COLUMN_3D | Represents a 3D Column chart series. |
| COLUMN_3D_STACKED | Represents a 3D Stacked Column chart series. |
| COLUMN_3D_PERCENT_STACKED | Represents a 3D 100% Stacked Column chart series. |
| COLUMN_3D_CLUSTERED | Represents a 3D Clustered Column chart series. |
| DOUGHNUT | Represents a Doughnut chart series. |
| LINE | Represents a Line chart series. |
| LINE_STACKED | Represents a Stacked Line chart series. |
| LINE_PERCENT_STACKED | Represents a 100% Stacked Line chart series. |
| LINE_3D | Represents a 3D Line chart series. |
| PIE | Represents a Pie chart series. |
| PIE_3D | Represents a 3D Pie chart series. |
| PIE_OF_BAR | Represents a Pie of Bar chart series. |
| PIE_OF_PIE | Represents a Pie of Pie chart series. |
| RADAR | Represents a Radar chart series. |
| SCATTER | Represents a Scatter chart series. |
| STOCK | Represents a Stock chart series. |
| SURFACE | Represents a Surface chart series. |
| SURFACE_3D | Represents a 3D Surface chart series. |
| TREEMAP | Represents a Treemap chart series. |
| SUNBURST | Represents a Sunburst chart series. |
| HISTOGRAM | Represents a Histogram chart series. |
| PARETO | Represents a Pareto chart series. |
| PARETO_LINE | Represents a Pareto Line chart series. |
| BOX_AND_WHISKER | Represents a Box and Whisker chart series. |
| WATERFALL | Represents a Waterfall chart series. |
| FUNNEL | Represents a Funnel chart series. |
| REGION_MAP | Represents a Region Map chart series. |

### Examples

Shows how to remove specific chart serie.

```python
doc = aw.Document(file_name=MY_DIR + 'Reporting engine template - Chart series.docx')
chart = doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape().chart
# Remove all series of the Column type.
i = chart.series.count - 1
while i >= 0:
    if chart.series[i].series_type == aw.drawing.charts.ChartSeriesType.COLUMN:
        chart.series.remove_at(i)
    i -= 1
chart.series.add1(series_name='Aspose Series', categories=['Category 1', 'Category 2', 'Category 3', 'Category 4'], values=[5.6, 7.1, 2.9, 8.9])
doc.save(file_name=ARTIFACTS_DIR + 'Charts.RemoveSpecificChartSeries.docx')
```

### See Also

* module [aspose.words.drawing.charts](../)

