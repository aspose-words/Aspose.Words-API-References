---
title: AxisBound class
linktitle: AxisBound class
articleTitle: AxisBound class
second_title: Aspose.Words for Python
description: "aspose.words.drawing.charts.AxisBound class. Represents minimum or maximum bound of axis values"
type: docs
weight: 10
url: /es/python-net/aspose.words.drawing.charts/axisbound/
---

## AxisBound class

Represents minimum or maximum bound of axis values.
To learn more, visit the [Working with Charts](https://docs.aspose.com/words/python-net/working-with-charts/) documentation article.




### Remarks

Bound can be specified as a numeric, datetime or a special "auto" value.

The instances of this class are immutable.




### Constructors
| Name | Description |
| --- | --- |
| [AxisBound()](./__init__/#default) | Creates a new instance indicating that axis bound should be determined automatically by a word-processing application. |
| [AxisBound(value)](./__init__/#float) | Creates an axis bound represented as a number. |
| [AxisBound(datetime)](./__init__/#datetime) | Creates an axis bound represented as datetime value. |

### Properties

| Name | Description |
| --- | --- |
| [is_auto](./is_auto/) | Returns a flag indicating that axis bound should be determined automatically. |
| [value](./value/) | Returns numeric value of axis bound. |
| [value_as_date](./value_as_date/) | Returns value of axis bound represented as datetime. |

### Examples

Shows how to insert chart with date/time values.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.LINE, width=500, height=300)
chart = shape.chart
# Limpia las series de datos de demostración del gráfico para comenzar con un gráfico limpio.
chart.series.clear()
# Añade una serie personalizada que contenga valores de fecha/hora para el eje X, y valores decimales correspondientes para el eje Y.
chart.series.add_date(series_name='Aspose Test Series', dates=[datetime.datetime(2017, 11, 6), datetime.datetime(2017, 11, 9), datetime.datetime(2017, 11, 15), datetime.datetime(2017, 11, 21), datetime.datetime(2017, 11, 25), datetime.datetime(2017, 11, 29)], values=[1.2, 0.3, 2.1, 2.9, 4.2, 5.3])
# Establece los límites inferior y superior para el eje X.
x_axis = chart.axis_x
# Convierte datetime a fecha de OLE Automation (días desde 1899-12-30)

def to_ole_autodate(dt):
    # Los días desde 0001-01-01 hasta 1899-12-30 son 693594
    delta = dt - datetime.datetime(1899, 12, 30)
    return delta.days + (dt.hour * 3600 + dt.minute * 60 + dt.second) / 86400.0
x_axis.scaling.minimum = aw.drawing.charts.AxisBound(to_ole_autodate(datetime.datetime(2017, 11, 5)))
x_axis.scaling.maximum = aw.drawing.charts.AxisBound(to_ole_autodate(datetime.datetime(2017, 12, 3)))
# Establece las unidades mayores del eje X a una semana, y las unidades menores a un día.
x_axis.base_time_unit = aw.drawing.charts.AxisTimeUnit.DAYS
x_axis.major_unit = 7
x_axis.major_tick_mark = aw.drawing.charts.AxisTickMark.CROSS
x_axis.minor_unit = 1
x_axis.minor_tick_mark = aw.drawing.charts.AxisTickMark.OUTSIDE
x_axis.has_major_gridlines = True
x_axis.has_minor_gridlines = True
# Define las propiedades del eje Y para valores decimales.
y_axis = chart.axis_y
y_axis.tick_labels.position = aw.drawing.charts.AxisTickLabelPosition.HIGH
y_axis.major_unit = 100
y_axis.minor_unit = 50
y_axis.display_unit.unit = aw.drawing.charts.AxisBuiltInUnit.HUNDREDS
y_axis.scaling.minimum = aw.drawing.charts.AxisBound(100)
y_axis.scaling.maximum = aw.drawing.charts.AxisBound(700)
y_axis.has_major_gridlines = True
y_axis.has_minor_gridlines = True
doc.save(file_name=ARTIFACTS_DIR + 'Charts.DateTimeValues.docx')
```

### See Also

* module [aspose.words.drawing.charts](../)
* property [AxisScaling.minimum](../axisscaling/minimum/)
* property [AxisScaling.maximum](../axisscaling/maximum/)

