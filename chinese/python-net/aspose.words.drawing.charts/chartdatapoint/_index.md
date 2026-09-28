---
title: ChartDataPoint class
linktitle: ChartDataPoint class
articleTitle: ChartDataPoint class
second_title: Aspose.Words for Python
description: "aspose.words.drawing.charts.ChartDataPoint class. Allows to specify formatting of a single data point on the chart"
type: docs
weight: 230
url: /zh/python-net/aspose.words.drawing.charts/chartdatapoint/
---

## ChartDataPoint class

Allows to specify formatting of a single data point on the chart.
To learn more, visit the [Working with Charts](https://docs.aspose.com/words/python-net/working-with-charts/) documentation article.




### Remarks

On a series, the [ChartDataPoint](./) object is a member of the [ChartDataPointCollection](../chartdatapointcollection/). 
The [ChartDataPointCollection](../chartdatapointcollection/) contains a [ChartDataPoint](./) object for each point. 



**Interfaces:** [IChartDataPoint](../ichartdatapoint/)

### Properties

| Name | Description |
| --- | --- |
| [bubble_3d](./bubble_3d/) | Specifies whether the bubbles in Bubble chart should have a 3-D effect applied to them. |
| [explosion](./explosion/) | Specifies the amount the data point shall be moved from the center of the pie. Can be negative, negative means that property is not set and no explosion should be applied. Applies only to Pie charts. |
| [format](./format/) | Provides access to fill and line formatting of this data point. |
| [index](./index/) | Index of the data point this object applies formatting to. |
| [invert_if_negative](./invert_if_negative/) | Specifies whether the parent element shall inverts its colors if the value is negative. |
| [marker](./marker/) | Specifies chart data marker. |

### Methods

| Name | Description |
| --- | --- |
|[ clear_format()](./clear_format/#default) | Clears format of this data point. The properties are set to the default values defined in the parent series. |

### Examples

Shows how to work with data points on a line chart.

```python
from api_example_base import ApiExampleBase, ARTIFACTS_DIR
import aspose.words as aw
import aspose.pydrawing as drawing
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.LINE, width=500, height=350)
chart = shape.chart
self.assertEqual(3, chart.series.count)
self.assertEqual('Series 1', chart.series[0].name)
self.assertEqual('Series 2', chart.series[1].name)
self.assertEqual('Series 3', chart.series[2].name)
# 通过将图表的数据点显示为菱形来强调它们。
for series in chart.series:
    ExCharts._apply_data_points(series, 4, aw.drawing.charts.MarkerSymbol.DIAMOND, 15)
# 平滑表示第一数据系列的线条。
chart.series[0].smooth = True
# 验证第一系列的数据点在数值为负时不会反转颜色。
for data_point in chart.series[0].data_points:
    assert not data_point.invert_if_negative
data_point = chart.series[1].data_points[2]
data_point.format.fill.color = drawing.Color.red
# 为了获得更简洁的图形，我们可以单独清除格式。
data_point.clear_format()
# 我们也可以一次性清除整条数据系列的所有点。
chart.series[2].data_points.clear_format()
doc.save(file_name=ARTIFACTS_DIR + 'Charts.ChartDataPoint.docx')
```

Shows how to work with data points on a line chart (ApplyDataPoints).

```python
@staticmethod
def _apply_data_points(series, data_points_count, marker_symbol, data_point_size):
    i = 0
    while i < data_points_count:
        point = series.data_points[i]
        point.marker.symbol = marker_symbol
        point.marker.size = data_point_size
        assert i == point.index
        i += 1
```

### See Also

* module [aspose.words.drawing.charts](../)
* class [IChartDataPoint](../ichartdatapoint/)

