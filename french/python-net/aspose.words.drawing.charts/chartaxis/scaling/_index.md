---
title: ChartAxis.scaling property
linktitle: scaling property
articleTitle: scaling property
second_title: Aspose.Words for Python
description: "ChartAxis.scaling property. Provides access to the scaling options of the axis."
type: docs
weight: 220
url: /fr/python-net/aspose.words.drawing.charts/chartaxis/scaling/
---

## ChartAxis.scaling property

Provides access to the scaling options of the axis.


```python
@property
def scaling(self) -> aspose.words.drawing.charts.AxisScaling:
    ...

```

### Examples

Shows how to insert chart with date/time values.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.LINE, width=500, height=300)
chart = shape.chart
# Effacez les séries de données de démonstration du graphique pour commencer avec un graphique vierge.
chart.series.clear()
# Ajoutez une série personnalisée contenant des valeurs date/heure pour l'axe X, et des valeurs décimales respectives pour l'axe Y.
chart.series.add_date(series_name='Aspose Test Series', dates=[datetime.datetime(2017, 11, 6), datetime.datetime(2017, 11, 9), datetime.datetime(2017, 11, 15), datetime.datetime(2017, 11, 21), datetime.datetime(2017, 11, 25), datetime.datetime(2017, 11, 29)], values=[1.2, 0.3, 2.1, 2.9, 4.2, 5.3])
# Définissez les limites inférieure et supérieure pour l'axe X.
x_axis = chart.axis_x
# Convertissez la date/heure en date OLE Automation (jours depuis le 30‑12‑1899)

def to_ole_autodate(dt):
    # Le nombre de jours du 01‑01‑0001 au 30‑12‑1899 est 693594
    delta = dt - datetime.datetime(1899, 12, 30)
    return delta.days + (dt.hour * 3600 + dt.minute * 60 + dt.second) / 86400.0
x_axis.scaling.minimum = aw.drawing.charts.AxisBound(to_ole_autodate(datetime.datetime(2017, 11, 5)))
x_axis.scaling.maximum = aw.drawing.charts.AxisBound(to_ole_autodate(datetime.datetime(2017, 12, 3)))
# Définissez les unités majeures de l'axe X sur une semaine, et les unités mineures sur un jour.
x_axis.base_time_unit = aw.drawing.charts.AxisTimeUnit.DAYS
x_axis.major_unit = 7
x_axis.major_tick_mark = aw.drawing.charts.AxisTickMark.CROSS
x_axis.minor_unit = 1
x_axis.minor_tick_mark = aw.drawing.charts.AxisTickMark.OUTSIDE
x_axis.has_major_gridlines = True
x_axis.has_minor_gridlines = True
# Définissez les propriétés de l'axe Y pour les valeurs décimales.
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

* module [aspose.words.drawing.charts](../../)
* class [ChartAxis](../)

