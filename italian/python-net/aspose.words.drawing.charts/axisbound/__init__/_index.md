---
title: AxisBound constructor
linktitle: AxisBound constructor
articleTitle: AxisBound constructor
second_title: Aspose.Words for Python
description: "aspose.words.drawing.charts.AxisBound constructor"
type: docs
weight: 10
url: /it/python-net/aspose.words.drawing.charts/axisbound/__init__/
---

## AxisBound() {#default}

Creates a new instance indicating that axis bound should be determined automatically by a word-processing
application.


```python
def __init__(self):
    ...
```

## AxisBound(value) {#float}

Creates an axis bound represented as a number.


```python
def __init__(self, value: float):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| value | float |  |

## AxisBound(datetime) {#datetime}

Creates an axis bound represented as datetime value.


```python
def __init__(self, datetime: datetime.datetime):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| datetime | datetime.datetime |  |

## Examples

Shows how to insert chart with date/time values.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.LINE, width=500, height=300)
chart = shape.chart
# Cancella le serie di dati demo del grafico per iniziare con un grafico pulito.
chart.series.clear()
# Aggiungi una serie personalizzata contenente valori data/ora per l'asse X e valori decimali corrispondenti per l'asse Y.
chart.series.add_date(series_name='Aspose Test Series', dates=[datetime.datetime(2017, 11, 6), datetime.datetime(2017, 11, 9), datetime.datetime(2017, 11, 15), datetime.datetime(2017, 11, 21), datetime.datetime(2017, 11, 25), datetime.datetime(2017, 11, 29)], values=[1.2, 0.3, 2.1, 2.9, 4.2, 5.3])
# Imposta i limiti inferiore e superiore per l'asse X.
x_axis = chart.axis_x
# Converti data/ora in data OLE Automation (giorni dal 30-12-1899)

def to_ole_autodate(dt):
    # I giorni dal 01-01-0001 al 30-12-1899 sono 693594
    delta = dt - datetime.datetime(1899, 12, 30)
    return delta.days + (dt.hour * 3600 + dt.minute * 60 + dt.second) / 86400.0
x_axis.scaling.minimum = aw.drawing.charts.AxisBound(to_ole_autodate(datetime.datetime(2017, 11, 5)))
x_axis.scaling.maximum = aw.drawing.charts.AxisBound(to_ole_autodate(datetime.datetime(2017, 12, 3)))
# Imposta le unità principali dell'asse X a una settimana e le unità secondarie a un giorno.
x_axis.base_time_unit = aw.drawing.charts.AxisTimeUnit.DAYS
x_axis.major_unit = 7
x_axis.major_tick_mark = aw.drawing.charts.AxisTickMark.CROSS
x_axis.minor_unit = 1
x_axis.minor_tick_mark = aw.drawing.charts.AxisTickMark.OUTSIDE
x_axis.has_major_gridlines = True
x_axis.has_minor_gridlines = True
# Definisci le proprietà dell'asse Y per valori decimali.
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

## See Also

* module [aspose.words.drawing.charts](../../)
* class [AxisBound](../)

