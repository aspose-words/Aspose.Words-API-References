---
title: ChartSeries.copy_format_from method
linktitle: copy_format_from method
articleTitle: copy_format_from method
second_title: Aspose.Words for Python
description: "ChartSeries.copy_format_from method. Copies default data point format from the data point with the specified index."
type: docs
weight: 190
url: /zh/python-net/aspose.words.drawing.charts/chartseries/copy_format_from/
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
# 获取图表和系列以更新格式。
shape = doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape()
series = shape.chart.series[0]
data_points = series.data_points
self.assertTrue(data_points.has_default_format(0))
self.assertFalse(data_points.has_default_format(1))
# 将索引为 1 的数据点的格式复制到索引为 2 的数据点。
# 使数据点 2 看起来与数据点 1 相同。
data_points.copy_format(0, 1)
self.assertTrue(data_points.has_default_format(0))
self.assertTrue(data_points.has_default_format(1))
# 将索引为 0 的数据点的格式复制到系列默认设置，以便所有数据点
# 在具有默认格式的系列中，看起来与数据点 0 相同。
series.copy_format_from(1)
self.assertTrue(data_points.has_default_format(0))
self.assertTrue(data_points.has_default_format(1))
doc.save(file_name=ARTIFACTS_DIR + 'Charts.CopyDataPointFormat.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartSeries](../)

