﻿---
title: MarkerSymbol enumeration
linktitle: MarkerSymbol enumeration
articleTitle: MarkerSymbol enumeration
second_title: Aspose.Words for Python
description: "aspose.words.drawing.charts.MarkerSymbol enumeration. Specifies marker symbol style."
type: docs
weight: 500
url: /python-net/aspose.words.drawing.charts/markersymbol/
---

## MarkerSymbol enumeration

Specifies marker symbol style.


### Members

| Name | Description |
| --- | --- |
| DEFAULT | Specifies a default marker symbol shall be drawn at each data point. |
| CIRCLE | Specifies a circle shall be drawn at each data point. |
| DASH | Specifies a dash shall be drawn at each data point. |
| DIAMOND | Specifies a diamond shall be drawn at each data point. |
| DOT | Specifies a dot shall be drawn at each data point. |
| NONE | Specifies nothing shall be drawn at each data point. |
| PICTURE | Specifies a picture shall be drawn at each data point. |
| PLUS | Specifies a plus shall be drawn at each data point. |
| SQUARE | Specifies a square shall be drawn at each data point. |
| STAR | Specifies a star shall be drawn at each data point. |
| TRIANGLE | Specifies a triangle shall be drawn at each data point. |
| X | Specifies an X shall be drawn at each data point. |

### Examples

Shows how to work with data points on a line chart.

```python
def chart_data_point():
    doc = aw.Document()
    builder = aw.DocumentBuilder(doc)
    shape = builder.insert_chart(aw.drawing.charts.ChartType.LINE, 500, 350)
    chart = shape.chart
    self.assertEqual(3, chart.series.count)
    self.assertEqual('Series 1', chart.series[0].name)
    self.assertEqual('Series 2', chart.series[1].name)
    self.assertEqual('Series 3', chart.series[2].name)
    # Emphasize the chart's data points by making them appear as diamond shapes.
    for series in chart.series:
        apply_data_points(series, 4, aw.drawing.charts.MarkerSymbol.DIAMOND, 15)
    # Smooth out the line that represents the first data series.
    chart.series[0].smooth = True
    # Verify that data points for the first series will not invert their colors if the value is negative.
    for data_point in chart.series[0].data_points:
        self.assertFalse(data_point.invert_if_negative)
    # For a cleaner looking graph, we can clear format individually.
    chart.series[1].data_points[2].clear_format()
    # We can also strip an entire series of data points at once.
    chart.series[2].data_points.clear_format()
    doc.save(ARTIFACTS_DIR + 'Charts.chart_data_point.docx')

def apply_data_points(series: aw.drawing.charts.ChartSeries, data_points_count: int, marker_symbol: aw.drawing.charts.MarkerSymbol, data_point_size: int):
    """Applies a number of data points to a series."""
    for i in range(data_points_count):
        point = series.data_points[i]
        point.marker.symbol = marker_symbol
        point.marker.size = data_point_size
        self.assertEqual(i, point.index)
```

### See Also

* module [aspose.words.drawing.charts](../)

