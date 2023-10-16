---
title: ChartDataPointCollection.has_default_format method
linktitle: has_default_format method
articleTitle: has_default_format method
second_title: Aspose.Words for Python
description: "ChartDataPointCollection.has_default_format method. Gets a flag indicating whether the data point at the specified index has default format."
type: docs
weight: 50
url: /python-net/aspose.words.drawing.charts/chartdatapointcollection/has_default_format/
---

## has_default_format(data_point_index) {#int}

Gets a flag indicating whether the data point at the specified index has default format.


```python
def has_default_format(self, data_point_index: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| data_point_index | int |  |

### Examples

Shows how to copy data point format.

```python
doc = aw.Document(MY_DIR + "DataPoint format.docx")

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

doc.save(ARTIFACTS_DIR + "Charts.CopyDataPointFormat.docx")
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartDataPointCollection](../)

