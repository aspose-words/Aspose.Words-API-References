---
title: ChartDataPoint.format property
linktitle: format property
articleTitle: format property
second_title: Aspose.Words for Python
description: "ChartDataPoint.format property. Provides access to fill and line formatting of this data point."
type: docs
weight: 30
url: /it/python-net/aspose.words.drawing.charts/chartdatapoint/format/
---

## ChartDataPoint.format property

Provides access to fill and line formatting of this data point.


```python
@property
def format(self) -> aspose.words.drawing.charts.ChartFormat:
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

Shows how to set individual formatting for categories of a column chart.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.COLUMN, width=432, height=252)
chart = shape.chart
# Elimina la serie generata per impostazione predefinita.
chart.series.clear()
# Aggiunta di una nuova serie.
series = chart.series.add(series_name='Series 1', categories=['Category 1', 'Category 2', 'Category 3', 'Category 4'], values=[1, 2, 3, 4])
# Imposta la formattazione della colonna.
data_points = series.data_points
data_points[0].format.fill.preset_textured(aw.drawing.PresetTexture.DENIM)
data_points[1].format.fill.fore_color = aspose.pydrawing.Color.red
data_points[2].format.fill.fore_color = aspose.pydrawing.Color.yellow
data_points[3].format.fill.fore_color = aspose.pydrawing.Color.blue
doc.save(file_name=ARTIFACTS_DIR + 'Charts.DataPointsFormatting.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartDataPoint](../)

