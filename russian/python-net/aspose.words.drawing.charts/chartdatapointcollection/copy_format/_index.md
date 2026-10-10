---
title: ChartDataPointCollection.copy_format method
linktitle: copy_format method
articleTitle: copy_format method
second_title: Aspose.Words for Python
description: "ChartDataPointCollection.copy_format method. Copies format from the source data point to the destination data point."
type: docs
weight: 40
url: /ru/python-net/aspose.words.drawing.charts/chartdatapointcollection/copy_format/
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
# Получите диаграмму и серии для обновления формата.
shape = doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape()
series = shape.chart.series[0]
data_points = series.data_points
self.assertTrue(data_points.has_default_format(0))
self.assertFalse(data_points.has_default_format(1))
# Скопируйте формат точки данных с индексом 1 в точку данных с индексом 2
# чтобы точка данных 2 выглядела так же, как точка данных 1.
data_points.copy_format(0, 1)
self.assertTrue(data_points.has_default_format(0))
self.assertTrue(data_points.has_default_format(1))
# Скопировать формат точки данных с индексом 0 в значения по умолчанию серии, чтобы все точки данных
# в серии, имеющие формат по умолчанию, выглядели так же, как точка данных 0.
series.copy_format_from(1)
self.assertTrue(data_points.has_default_format(0))
self.assertTrue(data_points.has_default_format(1))
doc.save(file_name=ARTIFACTS_DIR + 'Charts.CopyDataPointFormat.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartDataPointCollection](../)

