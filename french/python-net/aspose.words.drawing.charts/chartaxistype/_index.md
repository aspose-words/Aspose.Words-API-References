---
title: ChartAxisType enumeration
linktitle: ChartAxisType enumeration
articleTitle: ChartAxisType enumeration
second_title: Aspose.Words for Python
description: "aspose.words.drawing.charts.ChartAxisType enumeration. Specifies type of chart axis."
type: docs
weight: 180
url: /fr/python-net/aspose.words.drawing.charts/chartaxistype/
---

## ChartAxisType enumeration

Specifies type of chart axis.


### Members

| Name | Description |
| --- | --- |
| CATEGORY | Category axis of a chart. |
| SERIES | Series axis of a chart. |
| VALUE | Value axis of a chart. |

### Examples

Shows how to create an appropriate type of chart series for a graph type.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Il existe plusieurs manières de remplir la collection de séries d'un graphique.
# Différents schémas de séries sont destinés à différents types de graphiques.
# 1 -  Diagramme à colonnes avec des colonnes groupées et bandées le long de l'axe X par catégorie:
chart = ExCharts._append_chart(builder, aw.drawing.charts.ChartType.COLUMN, 500, 300)
categories = ['Category 1', 'Category 2', 'Category 3']
# Insérez deux séries de valeurs décimales contenant une valeur pour chaque catégorie respective.
# Ce diagramme à colonnes comportera trois groupes, chacun avec deux colonnes.
chart.series.add(series_name='Series 1', categories=categories, values=[76.6, 82.1, 91.6])
chart.series.add(series_name='Series 2', categories=categories, values=[64.2, 79.5, 94])
# Les catégories sont réparties le long de l'axe X, et les valeurs le long de l'axe Y.
self.assertEqual(aw.drawing.charts.ChartAxisType.CATEGORY, chart.axis_x.type)
self.assertEqual(aw.drawing.charts.ChartAxisType.VALUE, chart.axis_y.type)
# 2 -  Diagramme en aires avec des dates réparties le long de l'axe X:
chart = ExCharts._append_chart(builder, aw.drawing.charts.ChartType.AREA, 500, 300)
dates = [datetime.datetime(2014, 3, 31), datetime.datetime(2017, 1, 23), datetime.datetime(2017, 6, 18), datetime.datetime(2019, 11, 22), datetime.datetime(2020, 9, 7)]
# Insérez une série avec une valeur décimale pour chaque date respective.
# Les dates seront réparties le long d'un axe X linéaire,
# et les valeurs ajoutées à cette série créeront des points de données.
chart.series.add_date(series_name='Series 1', dates=dates, values=[15.8, 21.5, 22.9, 28.7, 33.1])
self.assertEqual(aw.drawing.charts.ChartAxisType.CATEGORY, chart.axis_x.type)
self.assertEqual(aw.drawing.charts.ChartAxisType.VALUE, chart.axis_y.type)
# 3 -  Nuage de points 2D:
chart = ExCharts._append_chart(builder, aw.drawing.charts.ChartType.SCATTER, 500, 300)
# Chaque série nécessitera deux tableaux décimaux de même longueur.
# Le premier tableau contient les valeurs X, et le deuxième contient les valeurs Y correspondantes
# des points de données sur le graphique du diagramme.
chart.series.add_double(series_name='Series 1', x_values=[3.1, 3.5, 6.3, 4.1, 2.2, 8.3, 1.2, 3.6], y_values=[3.1, 6.3, 4.6, 0.9, 8.5, 4.2, 2.3, 9.9])
chart.series.add_double(series_name='Series 2', x_values=[2.6, 7.3, 4.5, 6.6, 2.1, 9.3, 0.7, 3.3], y_values=[7.1, 6.6, 3.5, 7.8, 7.7, 9.5, 1.3, 4.6])
self.assertEqual(aw.drawing.charts.ChartAxisType.VALUE, chart.axis_x.type)
self.assertEqual(aw.drawing.charts.ChartAxisType.VALUE, chart.axis_y.type)
# 4 -  Diagramme à bulles :
chart = ExCharts._append_chart(builder, aw.drawing.charts.ChartType.BUBBLE, 500, 300)
# Chaque série nécessitera trois tableaux décimaux de même longueur.
# Le premier tableau contient les valeurs X, le deuxième contient les valeurs Y correspondantes,
# et le troisième contient les diamètres pour chaque point de données du graphique.
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

* module [aspose.words.drawing.charts](../)

