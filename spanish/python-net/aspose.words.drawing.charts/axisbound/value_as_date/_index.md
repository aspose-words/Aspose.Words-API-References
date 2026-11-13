---
title: AxisBound.value_as_date property
linktitle: value_as_date property
articleTitle: value_as_date property
second_title: Aspose.Words for Python
description: "AxisBound.value_as_date property. Returns value of axis bound represented as datetime."
type: docs
weight: 40
url: /es/python-net/aspose.words.drawing.charts/axisbound/value_as_date/
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
# Limpia las series de datos de demostración del gráfico para comenzar con un gráfico limpio.
chart.series.clear()
# Agregue una serie con dos matrices decimales. La primera matriz contiene los valores X,
# y la segunda contiene los valores Y correspondientes para los puntos en el gráfico de dispersión.
chart.series.add_double(series_name='Series 1', x_values=[1.1, 5.4, 7.9, 3.5, 2.1, 9.7], y_values=[2.1, 0.3, 0.6, 3.3, 1.4, 1.9])
# Por defecto, se aplica un escalado predeterminado a los ejes X e Y del gráfico,
# de modo que ambos rangos sean lo suficientemente amplios para abarcar cada valor X y Y de cada serie.
self.assertTrue(chart.axis_x.scaling.minimum.is_auto)
# Podemos definir nuestros propios límites de eje.
# En este caso, haremos que ambos ejes X e Y muestren un rango de 0 a 10.
chart.axis_x.scaling.minimum = aw.drawing.charts.AxisBound(value=0)
chart.axis_x.scaling.maximum = aw.drawing.charts.AxisBound(value=10)
chart.axis_y.scaling.minimum = aw.drawing.charts.AxisBound(value=0)
chart.axis_y.scaling.maximum = aw.drawing.charts.AxisBound(value=10)
self.assertFalse(chart.axis_x.scaling.minimum.is_auto)
self.assertFalse(chart.axis_y.scaling.minimum.is_auto)
# Cree un gráfico de líneas con una serie que requiera un rango de fechas en el eje X y valores decimales para el eje Y.
chart_shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.LINE, width=450, height=300)
chart = chart_shape.chart
chart.series.clear()
dates = [datetime.datetime(1973, 5, 11), datetime.datetime(1981, 2, 4), datetime.datetime(1985, 9, 23), datetime.datetime(1989, 6, 28), datetime.datetime(1994, 12, 15)]
chart.series.add_date(series_name='Series 1', dates=dates, values=[3, 4.7, 5.9, 7.1, 8.9])
# También podemos establecer límites de eje en forma de fechas, limitando el gráfico a un período.
# Establecer el rango a 1980-1990 omitirá dos de los valores de la serie
# que están fuera del rango del gráfico.
chart.axis_x.scaling.minimum = aw.drawing.charts.AxisBound(datetime=datetime.datetime(1980, 1, 1))
chart.axis_x.scaling.maximum = aw.drawing.charts.AxisBound(datetime=datetime.datetime(1990, 1, 1))
doc.save(file_name=ARTIFACTS_DIR + 'Charts.AxisBound.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [AxisBound](../)

