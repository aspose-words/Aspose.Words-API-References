---
title: ChartAxis.type property
linktitle: type property
articleTitle: type property
second_title: Aspose.Words for Python
description: "ChartAxis.type property. Returns type of the axis."
type: docs
weight: 260
url: /de/python-net/aspose.words.drawing.charts/chartaxis/type/
---

## ChartAxis.type property

Returns type of the axis.


```python
@property
def type(self) -> aspose.words.drawing.charts.ChartAxisType:
    ...

```

### Examples

Shows how to create an appropriate type of chart series for a graph type.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Es gibt mehrere Möglichkeiten, die Seriensammlung eines Diagramms zu füllen.
# Verschiedene Serienschemata sind für unterschiedliche Diagrammtypen vorgesehen.
# 1 -  Säulendiagramm mit nach Kategorie entlang der X-Achse gruppierten und bandierten Säulen:
chart = ExCharts._append_chart(builder, aw.drawing.charts.ChartType.COLUMN, 500, 300)
categories = ['Category 1', 'Category 2', 'Category 3']
# Fügen Sie zwei Serien von Dezimalwerten ein, die jeweils einen Wert für jede entsprechende Kategorie enthalten.
# Dieses Säulendiagramm wird drei Gruppen haben, jede mit zwei Säulen.
chart.series.add(series_name='Series 1', categories=categories, values=[76.6, 82.1, 91.6])
chart.series.add(series_name='Series 2', categories=categories, values=[64.2, 79.5, 94])
# Kategorien werden entlang der X-Achse verteilt, und Werte entlang der Y-Achse verteilt.
self.assertEqual(aw.drawing.charts.ChartAxisType.CATEGORY, chart.axis_x.type)
self.assertEqual(aw.drawing.charts.ChartAxisType.VALUE, chart.axis_y.type)
# 2 -  Flächendiagramm mit Daten, die entlang der X-Achse verteilt sind:
chart = ExCharts._append_chart(builder, aw.drawing.charts.ChartType.AREA, 500, 300)
dates = [datetime.datetime(2014, 3, 31), datetime.datetime(2017, 1, 23), datetime.datetime(2017, 6, 18), datetime.datetime(2019, 11, 22), datetime.datetime(2020, 9, 7)]
# Fügen Sie eine Serie mit einem Dezimalwert für jedes entsprechende Datum ein.
# Die Daten werden entlang einer linearen X-Achse verteilt,
# und die zu dieser Serie hinzugefügten Werte werden Datenpunkte erzeugen.
chart.series.add_date(series_name='Series 1', dates=dates, values=[15.8, 21.5, 22.9, 28.7, 33.1])
self.assertEqual(aw.drawing.charts.ChartAxisType.CATEGORY, chart.axis_x.type)
self.assertEqual(aw.drawing.charts.ChartAxisType.VALUE, chart.axis_y.type)
# 3 -  2D-Streudiagramm:
chart = ExCharts._append_chart(builder, aw.drawing.charts.ChartType.SCATTER, 500, 300)
# Jede Serie benötigt zwei Dezimal-Arrays gleicher Länge.
# Das erste Array enthält X-Werte, und das zweite enthält die entsprechenden Y-Werte
# von Datenpunkten im Diagrammgraphen.
chart.series.add_double(series_name='Series 1', x_values=[3.1, 3.5, 6.3, 4.1, 2.2, 8.3, 1.2, 3.6], y_values=[3.1, 6.3, 4.6, 0.9, 8.5, 4.2, 2.3, 9.9])
chart.series.add_double(series_name='Series 2', x_values=[2.6, 7.3, 4.5, 6.6, 2.1, 9.3, 0.7, 3.3], y_values=[7.1, 6.6, 3.5, 7.8, 7.7, 9.5, 1.3, 4.6])
self.assertEqual(aw.drawing.charts.ChartAxisType.VALUE, chart.axis_x.type)
self.assertEqual(aw.drawing.charts.ChartAxisType.VALUE, chart.axis_y.type)
# 4 -  Blasendiagramm:
chart = ExCharts._append_chart(builder, aw.drawing.charts.ChartType.BUBBLE, 500, 300)
# Jede Serie benötigt drei Dezimal-Arrays gleicher Länge.
# Das erste Array enthält X-Werte, das zweite enthält die entsprechenden Y-Werte,
# und das dritte enthält Durchmesser für jeden Datenpunkt des Diagramms.
chart.series.add_bubbles(series_name='Series 1', x_values=[1.1, 5, 9.8], y_values=[1.2, 4.9, 9.9], bubble_sizes=[2, 4, 8])
doc.save(file_name=ARTIFACTS_DIR + 'Charts.ChartSeriesCollection.docx')
```

Shows how to create an appropriate type of chart series for a graph type (AppendChart).

```python
@staticmethod
def _append_chart(builder, chart_type, width, height):
    chart_shape = builder.insert_chart(chart_type=chart_type, width=width, height=height)
    chart = chart_shape.chart
    chart.series.clear()
    return chart
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartAxis](../)

