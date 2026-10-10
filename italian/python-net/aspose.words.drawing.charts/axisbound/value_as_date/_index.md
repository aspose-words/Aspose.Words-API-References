---
title: AxisBound.value_as_date property
linktitle: value_as_date property
articleTitle: value_as_date property
second_title: Aspose.Words for Python
description: "AxisBound.value_as_date property. Returns value of axis bound represented as datetime."
type: docs
weight: 40
url: /it/python-net/aspose.words.drawing.charts/axisbound/value_as_date/
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
# Cancella le serie di dati demo del grafico per iniziare con un grafico pulito.
chart.series.clear()
# Aggiungi una serie con due array decimali. Il primo array contiene i valori X,
# e il secondo contiene i valori Y corrispondenti per i punti nel grafico a dispersione.
chart.series.add_double(series_name='Series 1', x_values=[1.1, 5.4, 7.9, 3.5, 2.1, 9.7], y_values=[2.1, 0.3, 0.6, 3.3, 1.4, 1.9])
# Per impostazione predefinita, viene applicata la scala predefinita agli assi X e Y del grafico,
# in modo che entrambi i loro intervalli siano sufficientemente ampi da includere ogni valore X e Y di ogni serie.
self.assertTrue(chart.axis_x.scaling.minimum.is_auto)
# Possiamo definire i nostri limiti degli assi.
# In questo caso, faremo in modo che entrambi gli assi X e Y mostrino un intervallo da 0 a 10.
chart.axis_x.scaling.minimum = aw.drawing.charts.AxisBound(value=0)
chart.axis_x.scaling.maximum = aw.drawing.charts.AxisBound(value=10)
chart.axis_y.scaling.minimum = aw.drawing.charts.AxisBound(value=0)
chart.axis_y.scaling.maximum = aw.drawing.charts.AxisBound(value=10)
self.assertFalse(chart.axis_x.scaling.minimum.is_auto)
self.assertFalse(chart.axis_y.scaling.minimum.is_auto)
# Crea un grafico a linee con una serie che richiede un intervallo di date sull'asse X e valori decimali per l'asse Y.
chart_shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.LINE, width=450, height=300)
chart = chart_shape.chart
chart.series.clear()
dates = [datetime.datetime(1973, 5, 11), datetime.datetime(1981, 2, 4), datetime.datetime(1985, 9, 23), datetime.datetime(1989, 6, 28), datetime.datetime(1994, 12, 15)]
chart.series.add_date(series_name='Series 1', dates=dates, values=[3, 4.7, 5.9, 7.1, 8.9])
# Possiamo impostare i limiti degli assi anche sotto forma di date, limitando il grafico a un periodo.
# Impostare l'intervallo su 1980-1990 escluderà due dei valori della serie
# che sono al di fuori dell'intervallo del grafico.
chart.axis_x.scaling.minimum = aw.drawing.charts.AxisBound(datetime=datetime.datetime(1980, 1, 1))
chart.axis_x.scaling.maximum = aw.drawing.charts.AxisBound(datetime=datetime.datetime(1990, 1, 1))
doc.save(file_name=ARTIFACTS_DIR + 'Charts.AxisBound.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [AxisBound](../)

