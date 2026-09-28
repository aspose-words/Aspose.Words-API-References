---
title: ChartDataPointCollection.copy_format method
linktitle: copy_format method
articleTitle: copy_format method
second_title: Aspose.Words for Python
description: "ChartDataPointCollection.copy_format method. Copies format from the source data point to the destination data point."
type: docs
weight: 40
url: /zh/python-net/aspose.words.drawing.charts/chartdatapointcollection/copy_format/
---

## copy_format(source_index, destination_index) {#int_int}

Copies format from the source data point to the destination data point.


```python
def copy_format(self, source_index: int, destination_index: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| source_index | int |  |
| destination_index | int |  |

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
* class [ChartDataPointCollection](../)

