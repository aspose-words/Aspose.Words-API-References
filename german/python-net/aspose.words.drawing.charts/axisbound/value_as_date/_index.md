---
title: AxisBound.value_as_date property
linktitle: value_as_date property
articleTitle: value_as_date property
second_title: Aspose.Words for Python
description: "AxisBound.value_as_date property. Returns value of axis bound represented as datetime."
type: docs
weight: 40
url: /de/python-net/aspose.words.drawing.charts/axisbound/value_as_date/
---

## AxisBound.value_as_date property

Returns value of axis bound represented as datetime.


```python
@property
def value_as_date(self) -> datetime.datetime:
    ...

```

### Examples

Shows how to set custom axis bounds.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
chart_shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.SCATTER, width=450, height=300)
chart = chart_shape.chart
# Leeren Sie die Demo‑Datenserien des Diagramms, um mit einem leeren Diagramm zu beginnen.
chart.series.clear()
# Fügen Sie eine Serie mit zwei Dezimal-Arrays hinzu. Das erste Array enthält die X-values,
# und das zweite enthält die entsprechenden Y-values für Punkte im Streudiagramm.
chart.series.add_double(series_name='Series 1', x_values=[1.1, 5.4, 7.9, 3.5, 2.1, 9.7], y_values=[2.1, 0.3, 0.6, 3.3, 1.4, 1.9])
# Standardmäßig wird eine Standardskalierung auf die X- und Y-Achsen des Diagramms angewendet,
# so dass beide Bereiche groß genug sind, um jeden X- und Y-Wert jeder Serie zu umfassen.
self.assertTrue(chart.axis_x.scaling.minimum.is_auto)
# Wir können eigene Achsenbegrenzungen definieren.
# In diesem Fall lassen wir beide, die X- und Y-Achsen, einen Bereich von 0 bis 10 anzeigen.
chart.axis_x.scaling.minimum = aw.drawing.charts.AxisBound(value=0)
chart.axis_x.scaling.maximum = aw.drawing.charts.AxisBound(value=10)
chart.axis_y.scaling.minimum = aw.drawing.charts.AxisBound(value=0)
chart.axis_y.scaling.maximum = aw.drawing.charts.AxisBound(value=10)
self.assertFalse(chart.axis_x.scaling.minimum.is_auto)
self.assertFalse(chart.axis_y.scaling.minimum.is_auto)
# Erstellen Sie ein Liniendiagramm mit einer Serie, die einen Datumsbereich auf der X-Achse und Dezimalwerte für die Y-Achse erfordert.
chart_shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.LINE, width=450, height=300)
chart = chart_shape.chart
chart.series.clear()
dates = [datetime.datetime(1973, 5, 11), datetime.datetime(1981, 2, 4), datetime.datetime(1985, 9, 23), datetime.datetime(1989, 6, 28), datetime.datetime(1994, 12, 15)]
chart.series.add_date(series_name='Series 1', dates=dates, values=[3, 4.7, 5.9, 7.1, 8.9])
# Wir können Achsenbegrenzungen auch in Form von Daten festlegen und das Diagramm auf einen Zeitraum beschränken.
# Das Festlegen des Bereichs auf 1980-1990 lässt die beiden Werte der Serie weg
# die außerhalb des Bereichs des Diagramms liegen.
chart.axis_x.scaling.minimum = aw.drawing.charts.AxisBound(datetime=datetime.datetime(1980, 1, 1))
chart.axis_x.scaling.maximum = aw.drawing.charts.AxisBound(datetime=datetime.datetime(1990, 1, 1))
doc.save(file_name=ARTIFACTS_DIR + 'Charts.AxisBound.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [AxisBound](../)

