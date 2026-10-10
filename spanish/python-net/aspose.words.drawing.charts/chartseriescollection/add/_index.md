---
title: ChartSeriesCollection.add method
linktitle: add method
articleTitle: add method
second_title: Aspose.Words for Python
description: "aspose.words.drawing.charts.ChartSeriesCollection.add method"
type: docs
weight: 30
url: /es/python-net/aspose.words.drawing.charts/chartseriescollection/add/
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
# Hay varias formas de poblar la colección de series de un gráfico.
# Los diferentes esquemas de series están destinados a distintos tipos de gráficos.
# 1 -  Gráfico de columnas con columnas agrupadas y franjas a lo largo del eje X por categoría:
chart = ExCharts._append_chart(builder, aw.drawing.charts.ChartType.COLUMN, 500, 300)
categories = ['Category 1', 'Category 2', 'Category 3']
# Inserta dos series de valores decimales que contengan un valor para cada categoría correspondiente.
# Este gráfico de columnas tendrá tres grupos, cada uno con dos columnas.
chart.series.add(series_name='Series 1', categories=categories, values=[76.6, 82.1, 91.6])
chart.series.add(series_name='Series 2', categories=categories, values=[64.2, 79.5, 94])
# Las categorías se distribuyen a lo largo del eje X, y los valores se distribuyen a lo largo del eje Y.
self.assertEqual(aw.drawing.charts.ChartAxisType.CATEGORY, chart.axis_x.type)
self.assertEqual(aw.drawing.charts.ChartAxisType.VALUE, chart.axis_y.type)
# 2 -  Gráfico de áreas con fechas distribuidas a lo largo del eje X:
chart = ExCharts._append_chart(builder, aw.drawing.charts.ChartType.AREA, 500, 300)
dates = [datetime.datetime(2014, 3, 31), datetime.datetime(2017, 1, 23), datetime.datetime(2017, 6, 18), datetime.datetime(2019, 11, 22), datetime.datetime(2020, 9, 7)]
# Inserta una serie con un valor decimal para cada fecha correspondiente.
# Las fechas se distribuirán a lo largo de un eje X lineal,
# y los valores añadidos a esta serie crearán puntos de datos.
chart.series.add_date(series_name='Series 1', dates=dates, values=[15.8, 21.5, 22.9, 28.7, 33.1])
self.assertEqual(aw.drawing.charts.ChartAxisType.CATEGORY, chart.axis_x.type)
self.assertEqual(aw.drawing.charts.ChartAxisType.VALUE, chart.axis_y.type)
# 3 -  Diagrama de dispersión 2D:
chart = ExCharts._append_chart(builder, aw.drawing.charts.ChartType.SCATTER, 500, 300)
# Cada serie necesitará dos matrices decimales de igual longitud.
# La primera matriz contiene valores X, y la segunda contiene los valores Y correspondientes
# de puntos de datos en el gráfico del diagrama.
chart.series.add_double(series_name='Series 1', x_values=[3.1, 3.5, 6.3, 4.1, 2.2, 8.3, 1.2, 3.6], y_values=[3.1, 6.3, 4.6, 0.9, 8.5, 4.2, 2.3, 9.9])
chart.series.add_double(series_name='Series 2', x_values=[2.6, 7.3, 4.5, 6.6, 2.1, 9.3, 0.7, 3.3], y_values=[7.1, 6.6, 3.5, 7.8, 7.7, 9.5, 1.3, 4.6])
self.assertEqual(aw.drawing.charts.ChartAxisType.VALUE, chart.axis_x.type)
self.assertEqual(aw.drawing.charts.ChartAxisType.VALUE, chart.axis_y.type)
# 4 -  Gráfico de burbujas:
chart = ExCharts._append_chart(builder, aw.drawing.charts.ChartType.BUBBLE, 500, 300)
# Cada serie necesitará tres matrices decimales de igual longitud.
# La primera matriz contiene valores X, la segunda contiene los valores Y correspondientes,
# y la tercera contiene diámetros para cada uno de los puntos de datos del gráfico.
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
# Inserte un gráfico de Pareto.
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.PARETO, width=450, height=450)
chart = shape.chart
chart.title.text = 'Best-Selling Car'
# Eliminar la serie generada por defecto.
chart.series.clear()
# Agregue una serie.
chart.series.add(series_name='Best-Selling Car', categories=['Tesla Model Y', 'Toyota Corolla', 'Toyota RAV4', 'Ford F-Series', 'Honda CR-V'], values=[1.43, 0.91, 1.17, 0.98, 0.85])
doc.save(file_name=ARTIFACTS_DIR + 'Charts.Pareto.docx')
```

Shows how to create box and whisker chart.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Inserte un gráfico de caja y bigotes.
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.BOX_AND_WHISKER, width=450, height=450)
chart = shape.chart
chart.title.text = 'Points by Years'
# Eliminar la serie generada por defecto.
chart.series.clear()
# Agregue una serie.
series = chart.series.add(series_name='Points by Years', categories=['WC', 'WC', 'WC', 'WC', 'WC', 'WC', 'WC', 'WC', 'WC', 'WC', 'NR', 'NR', 'NR', 'NR', 'NR', 'NR', 'NR', 'NR', 'NR', 'NR', 'NA', 'NA', 'NA', 'NA', 'NA', 'NA', 'NA', 'NA', 'NA', 'NA'], values=[91, 80, 100, 77, 90, 104, 105, 118, 120, 101, 114, 107, 110, 60, 79, 78, 77, 102, 101, 113, 94, 93, 84, 71, 80, 103, 80, 94, 100, 101])
# Mostrar etiquetas de datos.
series.has_data_labels = True
doc.save(file_name=ARTIFACTS_DIR + 'Charts.BoxAndWhisker.docx')
```

Shows how to create funnel chart.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
# Inserte un gráfico de embudo.
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.FUNNEL, width=450, height=450)
chart = shape.chart
chart.title.text = 'Population by Age Group'
# Eliminar la serie generada por defecto.
chart.series.clear()
# Agregue una serie.
series = chart.series.add(series_name='Population by Age Group', categories=['0-9', '10-19', '20-29', '30-39', '40-49', '50-59', '60-69', '70-79', '80-89', '90-'], values=[0.121, 0.128, 0.132, 0.146, 0.124, 0.124, 0.111, 0.075, 0.032, 0.007])
# Mostrar etiquetas de datos.
series.has_data_labels = True
decimal_separator = locale.localeconv()['decimal_point']
series.data_labels.number_format.format_code = f'0{decimal_separator}0%'
doc.save(file_name=ARTIFACTS_DIR + 'Charts.Funnel.docx')
```

Shows how to create waterfall chart.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Inserte un gráfico de cascada.
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.WATERFALL, width=450, height=450)
chart = shape.chart
chart.title.text = 'New Zealand GDP'
# Eliminar la serie generada por defecto.
chart.series.clear()
# Agregue una serie.
series = chart.series.add(series_name='New Zealand GDP', categories=['2018', '2019 growth', '2020 growth', '2020', '2021 growth', '2022 growth', '2022'], values=[100, 0.57, -0.25, 100.32, 20.22, -2.92, 117.62], is_subtotal=[True, False, False, True, False, False, True])
# Mostrar etiquetas de datos.
series.has_data_labels = True
doc.save(file_name=ARTIFACTS_DIR + 'Charts.Waterfall.docx')
```

## See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartSeriesCollection](../)

