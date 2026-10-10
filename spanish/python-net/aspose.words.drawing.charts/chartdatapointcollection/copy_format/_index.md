---
title: ChartDataPointCollection.copy_format method
linktitle: copy_format method
articleTitle: copy_format method
second_title: Aspose.Words for Python
description: "ChartDataPointCollection.copy_format method. Copies format from the source data point to the destination data point."
type: docs
weight: 40
url: /es/python-net/aspose.words.drawing.charts/chartdatapointcollection/copy_format/
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
# Obtenga el gráfico y la serie para actualizar el formato.
shape = doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape()
series = shape.chart.series[0]
data_points = series.data_points
self.assertTrue(data_points.has_default_format(0))
self.assertFalse(data_points.has_default_format(1))
# Copie el formato del punto de datos con índice 1 al punto de datos con índice 2
# para que el punto de datos 2 tenga el mismo aspecto que el punto de datos 1.
data_points.copy_format(0, 1)
self.assertTrue(data_points.has_default_format(0))
self.assertTrue(data_points.has_default_format(1))
# Copiar el formato del punto de datos con índice 0 a los valores predeterminados de la serie para que todos los puntos de datos
# en la serie que tienen el formato predeterminado tengan el mismo aspecto que el punto de datos 0.
series.copy_format_from(1)
self.assertTrue(data_points.has_default_format(0))
self.assertTrue(data_points.has_default_format(1))
doc.save(file_name=ARTIFACTS_DIR + 'Charts.CopyDataPointFormat.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartDataPointCollection](../)

