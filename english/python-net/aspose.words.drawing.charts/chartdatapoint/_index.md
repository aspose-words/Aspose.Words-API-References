﻿---
title: ChartDataPoint class
second_title: Aspose.Words for Python via .NET API Reference
description: "Allows to specify formatting of a single data point on the chart"
type: docs
weight: 180
url: /python-net/aspose.words.drawing.charts/chartdatapoint/
---

## ChartDataPoint class

Allows to specify formatting of a single data point on the chart.
To learn more, visit the [Working with Charts](https://docs.aspose.com/words/python-net/working-with-charts/) documentation article.




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
def test_chart_data_point(self):

    doc = aw.Document()
    builder = aw.DocumentBuilder(doc)

    shape = builder.insert_chart(aw.drawing.charts.ChartType.LINE, 500, 350)
    chart = shape.chart

    self.assertEqual(3, chart.series.count)
    self.assertEqual("Series 1", chart.series[0].name)
    self.assertEqual("Series 2", chart.series[1].name)
    self.assertEqual("Series 3", chart.series[2].name)

    # Emphasize the chart's data points by making them appear as diamond shapes.
    for series in chart.series:
        self.apply_data_points(series, 4, aw.drawing.charts.MarkerSymbol.DIAMOND, 15)

    # Smooth out the line that represents the first data series.
    chart.series[0].smooth = True

    # Verify that data points for the first series will not invert their colors if the value is negative.
    for data_point in chart.series[0].data_points:
        self.assertFalse(data_point.invert_if_negative)

    # For a cleaner looking graph, we can clear format individually.
    chart.series[1].data_points[2].clear_format()

    # We can also strip an entire series of data points at once.
    chart.series[2].data_points.clear_format()

    doc.save(ARTIFACTS_DIR + "Charts.chart_data_point.docx")

def apply_data_points(self, series: aw.drawing.charts.ChartSeries, data_points_count: int, marker_symbol: aw.drawing.charts.MarkerSymbol, data_point_size: int):
    """Applies a number of data points to a series."""

    for i in range(data_points_count):
        point = series.data_points[i]
        point.marker.symbol = marker_symbol
        point.marker.size = data_point_size

        self.assertEqual(i, point.index)
```

### See Also

* module [aspose.words.drawing.charts](../)
* class [IChartDataPoint](../ichartdatapoint/)

