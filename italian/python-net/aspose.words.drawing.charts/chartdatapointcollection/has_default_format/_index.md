---
title: ChartDataPointCollection.has_default_format method
linktitle: has_default_format method
articleTitle: has_default_format method
second_title: Aspose.Words for Python
description: "ChartDataPointCollection.has_default_format method. Gets a flag indicating whether the data point at the specified index has default format."
type: docs
weight: 50
url: /it/python-net/aspose.words.drawing.charts/chartdatapointcollection/has_default_format/
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
doc = aw.Document(file_name=MY_DIR + 'DataPoint format.docx')
# Fai aggiornare il formato del grafico e delle serie.
shape = doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape()
series = shape.chart.series[0]
data_points = series.data_points
self.assertTrue(data_points.has_default_format(0))
self.assertFalse(data_points.has_default_format(1))
# Copia il formato del punto dati con indice 1 al punto dati con indice 2
# in modo che il punto dati 2 abbia lo stesso aspetto del punto dati 1.
data_points.copy_format(0, 1)
self.assertTrue(data_points.has_default_format(0))
self.assertTrue(data_points.has_default_format(1))
# Copia il formato del punto dati con indice 0 nelle impostazioni predefinite della serie in modo che tutti i punti dati
# nella serie che hanno il formato predefinito abbiano lo stesso aspetto del punto dati 0.
series.copy_format_from(1)
self.assertTrue(data_points.has_default_format(0))
self.assertTrue(data_points.has_default_format(1))
doc.save(file_name=ARTIFACTS_DIR + 'Charts.CopyDataPointFormat.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartDataPointCollection](../)

