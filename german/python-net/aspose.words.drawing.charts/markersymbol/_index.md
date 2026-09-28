---
title: MarkerSymbol enumeration
linktitle: MarkerSymbol enumeration
articleTitle: MarkerSymbol enumeration
second_title: Aspose.Words for Python
description: "aspose.words.drawing.charts.MarkerSymbol enumeration. Specifies marker symbol style."
type: docs
weight: 500
url: /de/python-net/aspose.words.drawing.charts/markersymbol/
---

## MarkerSymbol enumeration

Specifies marker symbol style.


### Members

| Name | Description |
| --- | --- |
| DEFAULT | Specifies a default marker symbol shall be drawn at each data point. |
| CIRCLE | Specifies a circle shall be drawn at each data point. |
| DASH | Specifies a dash shall be drawn at each data point. |
| DIAMOND | Specifies a diamond shall be drawn at each data point. |
| DOT | Specifies a dot shall be drawn at each data point. |
| NONE | Specifies nothing shall be drawn at each data point. |
| PICTURE | Specifies a picture shall be drawn at each data point. |
| PLUS | Specifies a plus shall be drawn at each data point. |
| SQUARE | Specifies a square shall be drawn at each data point. |
| STAR | Specifies a star shall be drawn at each data point. |
| TRIANGLE | Specifies a triangle shall be drawn at each data point. |
| X | Specifies an X shall be drawn at each data point. |

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
# Betone die Datenpunkte des Diagramms, indem du sie als Rautformen darstellst.
for series in chart.series:
    ExCharts._apply_data_points(series, 4, aw.drawing.charts.MarkerSymbol.DIAMOND, 15)
# Glätte die Linie, die die erste Datenreihe darstellt.
chart.series[0].smooth = True
# Überprüfe, dass Datenpunkte der ersten Reihe ihre Farben nicht umkehren, wenn der Wert negativ ist.
for data_point in chart.series[0].data_points:
    assert not data_point.invert_if_negative
data_point = chart.series[1].data_points[2]
data_point.format.fill.color = drawing.Color.red
# Für ein saubereres Diagramm können wir das Format einzeln löschen.
data_point.clear_format()
# Wir können auch eine gesamte Datenreihe auf einmal entfernen.
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

