---
title: ChartAxisType enumeration
linktitle: ChartAxisType enumeration
articleTitle: ChartAxisType enumeration
second_title: Aspose.Words for Python
description: "aspose.words.drawing.charts.ChartAxisType enumeration. Specifies type of chart axis."
type: docs
weight: 180
url: /it/python-net/aspose.words.drawing.charts/chartaxistype/
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
# Esistono diversi modi per popolare la collezione di serie di un grafico.
# Schemi di serie diversi sono destinati a tipi di grafico differenti.
# 1 -  Grafico a colonne con colonne raggruppate e bande lungo l'asse X per categoria:
chart = ExCharts._append_chart(builder, aw.drawing.charts.ChartType.COLUMN, 500, 300)
categories = ['Category 1', 'Category 2', 'Category 3']
# Inserisci due serie di valori decimali contenenti un valore per ciascuna categoria rispettiva.
# Questo grafico a colonne avrà tre gruppi, ciascuno con due colonne.
chart.series.add(series_name='Series 1', categories=categories, values=[76.6, 82.1, 91.6])
chart.series.add(series_name='Series 2', categories=categories, values=[64.2, 79.5, 94])
# Le categorie sono distribuite lungo l'asse X e i valori sono distribuiti lungo l'asse Y.
self.assertEqual(aw.drawing.charts.ChartAxisType.CATEGORY, chart.axis_x.type)
self.assertEqual(aw.drawing.charts.ChartAxisType.VALUE, chart.axis_y.type)
# 2 -  Grafico ad area con date distribuite lungo l'asse X:
chart = ExCharts._append_chart(builder, aw.drawing.charts.ChartType.AREA, 500, 300)
dates = [datetime.datetime(2014, 3, 31), datetime.datetime(2017, 1, 23), datetime.datetime(2017, 6, 18), datetime.datetime(2019, 11, 22), datetime.datetime(2020, 9, 7)]
# Inserisci una serie con un valore decimale per ciascuna data rispettiva.
# Le date saranno distribuite lungo un asse X lineare,
# e i valori aggiunti a questa serie creeranno punti dati.
chart.series.add_date(series_name='Series 1', dates=dates, values=[15.8, 21.5, 22.9, 28.7, 33.1])
self.assertEqual(aw.drawing.charts.ChartAxisType.CATEGORY, chart.axis_x.type)
self.assertEqual(aw.drawing.charts.ChartAxisType.VALUE, chart.axis_y.type)
# 3 -  Grafico a dispersione 2D:
chart = ExCharts._append_chart(builder, aw.drawing.charts.ChartType.SCATTER, 500, 300)
# Ogni serie richiederà due array decimali di uguale lunghezza.
# Il primo array contiene i valori X, e il secondo contiene i valori Y corrispondenti
# dei punti dati sul grafico del diagramma.
chart.series.add_double(series_name='Series 1', x_values=[3.1, 3.5, 6.3, 4.1, 2.2, 8.3, 1.2, 3.6], y_values=[3.1, 6.3, 4.6, 0.9, 8.5, 4.2, 2.3, 9.9])
chart.series.add_double(series_name='Series 2', x_values=[2.6, 7.3, 4.5, 6.6, 2.1, 9.3, 0.7, 3.3], y_values=[7.1, 6.6, 3.5, 7.8, 7.7, 9.5, 1.3, 4.6])
self.assertEqual(aw.drawing.charts.ChartAxisType.VALUE, chart.axis_x.type)
self.assertEqual(aw.drawing.charts.ChartAxisType.VALUE, chart.axis_y.type)
# 4 -  Grafico a bolle:
chart = ExCharts._append_chart(builder, aw.drawing.charts.ChartType.BUBBLE, 500, 300)
# Ogni serie richiederà tre array decimali di uguale lunghezza.
# Il primo array contiene i valori X, il secondo contiene i valori Y corrispondenti,
# e il terzo contiene i diametri per ciascuno dei punti dati del grafico.
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

