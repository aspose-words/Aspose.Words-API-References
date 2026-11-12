---
title: ChartDataPointCollection.copy_format method
linktitle: copy_format method
articleTitle: copy_format method
second_title: Aspose.Words for Python
description: "ChartDataPointCollection.copy_format method. Copies format from the source data point to the destination data point."
type: docs
weight: 40
url: /tr/python-net/aspose.words.drawing.charts/chartdatapointcollection/copy_format/
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
# Grafiği ve seriyi biçimi güncellenmek üzere alın.
shape = doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape()
series = shape.chart.series[0]
data_points = series.data_points
self.assertTrue(data_points.has_default_format(0))
self.assertFalse(data_points.has_default_format(1))
# İndeks 1 olan veri noktasının biçimini, indeks 2 olan veri noktasına kopyalayın
# veri noktası 2'nin veri noktası 1 gibi görünmesi için.
data_points.copy_format(0, 1)
self.assertTrue(data_points.has_default_format(0))
self.assertTrue(data_points.has_default_format(1))
# Dizinin varsayılanlarına, indeks 0'lı veri noktasının biçimini kopyalayarak tüm veri noktalarının
# seride varsayılan biçime sahip tüm veri noktalarının veri noktası 0 gibi görünmesini sağlayın.
series.copy_format_from(1)
self.assertTrue(data_points.has_default_format(0))
self.assertTrue(data_points.has_default_format(1))
doc.save(file_name=ARTIFACTS_DIR + 'Charts.CopyDataPointFormat.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartDataPointCollection](../)

