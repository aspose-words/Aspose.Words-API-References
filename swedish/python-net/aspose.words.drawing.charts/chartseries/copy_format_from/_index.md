---
title: ChartSeries.copy_format_from method
linktitle: copy_format_from method
articleTitle: copy_format_from method
second_title: Aspose.Words for Python
description: "ChartSeries.copy_format_from method. Copies default data point format from the data point with the specified index."
type: docs
weight: 190
url: /sv/python-net/aspose.words.drawing.charts/chartseries/copy_format_from/
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
# Få diagrammet och serierna att uppdatera formatet.
shape = doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape()
series = shape.chart.series[0]
data_points = series.data_points
self.assertTrue(data_points.has_default_format(0))
self.assertFalse(data_points.has_default_format(1))
# Kopiera formatet för datapunkten med index 1 till datapunkten med index 2
# så att datapunkt 2 ser likadan ut som datapunkt 1.
data_points.copy_format(0, 1)
self.assertTrue(data_points.has_default_format(0))
self.assertTrue(data_points.has_default_format(1))
# Kopiera formatet för datapunkten med index 0 till seriens standardinställningar så att alla datapunkter
# i serien som har standardformatet ser likadana ut som datapunkt 0.
series.copy_format_from(1)
self.assertTrue(data_points.has_default_format(0))
self.assertTrue(data_points.has_default_format(1))
doc.save(file_name=ARTIFACTS_DIR + 'Charts.CopyDataPointFormat.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartSeries](../)

