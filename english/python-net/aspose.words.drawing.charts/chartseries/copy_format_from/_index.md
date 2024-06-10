---
title: ChartSeries.copy_format_from method
linktitle: copy_format_from method
articleTitle: copy_format_from method
second_title: Aspose.Words for Python
description: "ChartSeries.copy_format_from method. Copies default data point format from the data point with the specified index."
type: docs
weight: 190
url: /python-net/aspose.words.drawing.charts/chartseries/copy_format_from/
---

## copy_format_from(data_point_index) {#int}

Copies default data point format from the data point with the specified index.


```python
def copy_format_from(self, data_point_index: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| data_point_index | int |  |

### Examples

Shows how to copy data point format.

```python
doc = aw.Document(file_name=MY_DIR + 'DataPoint format.docx')
# Get the chart and series to update format.
shape = doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape()
series = shape.chart.series[0]
data_points = series.data_points
self.assertTrue(data_points.has_default_format(0))
self.assertFalse(data_points.has_default_format(1))
# Copy format of the data point with index 1 to the data point with index 2
# so that the data point 2 looks the same as the data point 1.
data_points.copy_format(0, 1)
self.assertTrue(data_points.has_default_format(0))
self.assertTrue(data_points.has_default_format(1))
# Copy format of the data point with index 0 to the series defaults so that all data points
# in the series that have the default format look the same as the data point 0.
series.copy_format_from(1)
self.assertTrue(data_points.has_default_format(0))
self.assertTrue(data_points.has_default_format(1))
doc.save(file_name=ARTIFACTS_DIR + 'Charts.CopyDataPointFormat.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartSeries](../)

