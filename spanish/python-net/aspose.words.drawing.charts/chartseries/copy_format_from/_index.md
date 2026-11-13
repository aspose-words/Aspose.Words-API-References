---
title: ChartSeries.copy_format_from method
linktitle: copy_format_from method
articleTitle: copy_format_from method
second_title: Aspose.Words for Python
description: "ChartSeries.copy_format_from method. Copies default data point format from the data point with the specified index."
type: docs
weight: 190
url: /es/python-net/aspose.words.drawing.charts/chartseries/copy_format_from/
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
* class [ChartSeries](../)

