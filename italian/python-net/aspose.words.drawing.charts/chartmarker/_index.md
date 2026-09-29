---
title: ChartMarker class
linktitle: ChartMarker class
articleTitle: ChartMarker class
second_title: Aspose.Words for Python
description: "aspose.words.drawing.charts.ChartMarker class. Represents a chart data marker"
type: docs
weight: 300
url: /it/python-net/aspose.words.drawing.charts/chartmarker/
---

## ChartMarker class

Represents a chart data marker.
To learn more, visit the [Working with Charts](https://docs.aspose.com/words/python-net/working-with-charts/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [format](./format/) | Provides access to fill and line formatting of this marker. |
| [size](./size/) | Gets or sets chart marker size. Default value is 7. |
| [symbol](./symbol/) | Gets or sets chart marker symbol. |

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
# Evidenzia i punti dati del grafico facendoli apparire a forma di diamante.
for series in chart.series:
    ExCharts._apply_data_points(series, 4, aw.drawing.charts.MarkerSymbol.DIAMOND, 15)
# Leviga la linea che rappresenta la prima serie di dati.
chart.series[0].smooth = True
# Verifica che i punti dati per la prima serie non invertano i loro colori se il valore è negativo.
for data_point in chart.series[0].data_points:
    assert not data_point.invert_if_negative
data_point = chart.series[1].data_points[2]
data_point.format.fill.color = drawing.Color.red
# Per un grafico dall'aspetto più pulito, possiamo cancellare il formato individualmente.
data_point.clear_format()
# Possiamo anche rimuovere un'intera serie di punti dati in una volta.
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

* module [aspose.words.drawing.charts](../)

