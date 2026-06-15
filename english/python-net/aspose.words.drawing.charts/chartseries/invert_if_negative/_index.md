---
title: ChartSeries.invert_if_negative property
linktitle: invert_if_negative property
articleTitle: invert_if_negative property
second_title: Aspose.Words for Python
description: "ChartSeries.invert_if_negative property. Specifies whether the parent element shall inverts its colors if the value is negative."
type: docs
weight: 80
url: /python-net/aspose.words.drawing.charts/chartseries/invert_if_negative/
---

## ChartSeries.invert_if_negative property

Specifies whether the parent element shall inverts its colors if the value is negative.


```python
@property
def invert_if_negative(self) -> bool:
    ...

@invert_if_negative.setter
def invert_if_negative(self, value: bool):
    ...

```

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
# Emphasize the chart's data points by making them appear as diamond shapes.
for series in chart.series:
    ExCharts._apply_data_points(series, 4, aw.drawing.charts.MarkerSymbol.DIAMOND, 15)
# Smooth out the line that represents the first data series.
chart.series[0].smooth = True
# Verify that data points for the first series will not invert their colors if the value is negative.
for data_point in chart.series[0].data_points:
    assert not data_point.invert_if_negative
data_point = chart.series[1].data_points[2]
data_point.format.fill.color = drawing.Color.red
# For a cleaner looking graph, we can clear format individually.
data_point.clear_format()
# We can also strip an entire series of data points at once.
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

* module [aspose.words.drawing.charts](../../)
* class [ChartSeries](../)

