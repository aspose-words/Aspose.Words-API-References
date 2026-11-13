---
title: ChartDataPoint.invert_if_negative property
linktitle: invert_if_negative property
articleTitle: invert_if_negative property
second_title: Aspose.Words for Python
description: "ChartDataPoint.invert_if_negative property. Specifies whether the parent element shall inverts its colors if the value is negative."
type: docs
weight: 50
url: /es/python-net/aspose.words.drawing.charts/chartdatapoint/invert_if_negative/
---

## ChartDataPoint.invert_if_negative property

Specifies whether the parent element shall inverts its colors if the value is negative.


```python
@property
def invert_if_negative(self) -> bool:
    ...

@invert_if_negative.setter
def invert_if_negative(self, value: bool):
    ...

```

### Examples

Shows how to work with data points on a line chart.

```python
from api_example_base import ApiExampleBase, ARTIFACTS_DIR
import aspose.words as aw
import aspose.pydrawing as drawing
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.LINE, width=500, height=350)
chart = shape.chart
self.assertEqual(3, chart.series.count)
self.assertEqual('Series 1', chart.series[0].name)
self.assertEqual('Series 2', chart.series[1].name)
self.assertEqual('Series 3', chart.series[2].name)
# Resaltar los puntos de datos del gráfico haciéndolos aparecer como formas de diamante.
for series in chart.series:
    ExCharts._apply_data_points(series, 4, aw.drawing.charts.MarkerSymbol.DIAMOND, 15)
# Suavizar la línea que representa la primera serie de datos.
chart.series[0].smooth = True
# Verificar que los puntos de datos de la primera serie no inviertan sus colores si el valor es negativo.
for data_point in chart.series[0].data_points:
    assert not data_point.invert_if_negative
data_point = chart.series[1].data_points[2]
data_point.format.fill.color = drawing.Color.red
# Para un gráfico de aspecto más limpio, podemos borrar el formato individualmente.
data_point.clear_format()
# También podemos eliminar una serie completa de puntos de datos de una sola vez.
chart.series[2].data_points.clear_format()
doc.save(file_name=ARTIFACTS_DIR + 'Charts.ChartDataPoint.docx')
```

Shows how to work with data points on a line chart (ApplyDataPoints).

```python
@staticmethod
def _apply_data_points(series, data_points_count, marker_symbol, data_point_size):
    i = 0
    while i < data_points_count:
        point = series.data_points[i]
        point.marker.symbol = marker_symbol
        point.marker.size = data_point_size
        assert i == point.index
        i += 1
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartDataPoint](../)

