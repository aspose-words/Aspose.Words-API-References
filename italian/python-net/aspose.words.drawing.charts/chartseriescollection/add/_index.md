---
title: ChartSeriesCollection.add method
linktitle: add method
articleTitle: add method
second_title: Aspose.Words for Python
description: "aspose.words.drawing.charts.ChartSeriesCollection.add method"
type: docs
weight: 30
url: /it/python-net/aspose.words.drawing.charts/chartseriescollection/add/
---

## add(series_name, categories, values) {#str_strlist_floatlist}

Adds new [ChartSeries](../../chartseries/) to this collection.
Use this method to add series to any type of Bar, Column, Line and Surface charts.



```python
def add(self, series_name: str, categories: List[str], values: List[float]):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| series_name | str |  |
| categories | List[str] |  |
| values | List[float] |  |

### Returns

Recently added [ChartSeries](../../chartseries/) object.


## add(series_name, categories, values, is_subtotal) {#str_strlist_floatlist_boollist}

Adds new [ChartSeries](../../chartseries/) to this collection.
Use this method to add series to Waterfall charts.



```python
def add(self, series_name: str, categories: List[str], values: List[float], is_subtotal: List[bool]):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| series_name | str | A name of the series to be added. |
| categories | List[str] | Category names for the X axis. |
| values | List[float] | Y-axis values. |
| is_subtotal | List[bool] | Values indicating whether the corresponding Y value is a subtotal. |

### Remarks

For chart types other than Waterfall, *isSubtotal* values are ignored.


### Returns

Recently added [ChartSeries](../../chartseries/) object.


## Examples

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

Shows how to create pareto chart.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Inserisci un grafico Pareto.
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.PARETO, width=450, height=450)
chart = shape.chart
chart.title.text = 'Best-Selling Car'
# Elimina la serie generata per impostazione predefinita.
chart.series.clear()
# Aggiungi una serie.
chart.series.add(series_name='Best-Selling Car', categories=['Tesla Model Y', 'Toyota Corolla', 'Toyota RAV4', 'Ford F-Series', 'Honda CR-V'], values=[1.43, 0.91, 1.17, 0.98, 0.85])
doc.save(file_name=ARTIFACTS_DIR + 'Charts.Pareto.docx')
```

Shows how to create box and whisker chart.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Inserisci un grafico a scatola e baffi.
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.BOX_AND_WHISKER, width=450, height=450)
chart = shape.chart
chart.title.text = 'Points by Years'
# Elimina la serie generata per impostazione predefinita.
chart.series.clear()
# Aggiungi una serie.
series = chart.series.add(series_name='Points by Years', categories=['WC', 'WC', 'WC', 'WC', 'WC', 'WC', 'WC', 'WC', 'WC', 'WC', 'NR', 'NR', 'NR', 'NR', 'NR', 'NR', 'NR', 'NR', 'NR', 'NR', 'NA', 'NA', 'NA', 'NA', 'NA', 'NA', 'NA', 'NA', 'NA', 'NA'], values=[91, 80, 100, 77, 90, 104, 105, 118, 120, 101, 114, 107, 110, 60, 79, 78, 77, 102, 101, 113, 94, 93, 84, 71, 80, 103, 80, 94, 100, 101])
# Mostra le etichette dei dati.
series.has_data_labels = True
doc.save(file_name=ARTIFACTS_DIR + 'Charts.BoxAndWhisker.docx')
```

Shows how to create funnel chart.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
# Inserisci un grafico a imbuto.
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.FUNNEL, width=450, height=450)
chart = shape.chart
chart.title.text = 'Population by Age Group'
# Elimina la serie generata per impostazione predefinita.
chart.series.clear()
# Aggiungi una serie.
series = chart.series.add(series_name='Population by Age Group', categories=['0-9', '10-19', '20-29', '30-39', '40-49', '50-59', '60-69', '70-79', '80-89', '90-'], values=[0.121, 0.128, 0.132, 0.146, 0.124, 0.124, 0.111, 0.075, 0.032, 0.007])
# Mostra le etichette dei dati.
series.has_data_labels = True
decimal_separator = locale.localeconv()['decimal_point']
series.data_labels.number_format.format_code = f'0{decimal_separator}0%'
doc.save(file_name=ARTIFACTS_DIR + 'Charts.Funnel.docx')
```

Shows how to create waterfall chart.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Inserisci un grafico a cascata.
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.WATERFALL, width=450, height=450)
chart = shape.chart
chart.title.text = 'New Zealand GDP'
# Elimina la serie generata per impostazione predefinita.
chart.series.clear()
# Aggiungi una serie.
series = chart.series.add(series_name='New Zealand GDP', categories=['2018', '2019 growth', '2020 growth', '2020', '2021 growth', '2022 growth', '2022'], values=[100, 0.57, -0.25, 100.32, 20.22, -2.92, 117.62], is_subtotal=[True, False, False, True, False, False, True])
# Mostra le etichette dei dati.
series.has_data_labels = True
doc.save(file_name=ARTIFACTS_DIR + 'Charts.Waterfall.docx')
```

## See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartSeriesCollection](../)

