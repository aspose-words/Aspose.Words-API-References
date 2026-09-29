---
title: ChartSeriesCollection class
linktitle: ChartSeriesCollection class
articleTitle: ChartSeriesCollection class
second_title: Aspose.Words for Python
description: "aspose.words.drawing.charts.ChartSeriesCollection class. Represents collection of a [ChartSeries](../chartseries/)"
type: docs
weight: 340
url: /es/python-net/aspose.words.drawing.charts/chartseriescollection/
---

## ChartSeriesCollection class

Represents collection of a [ChartSeries](../chartseries/).
To learn more, visit the [Working with Charts](https://docs.aspose.com/words/python-net/working-with-charts/) documentation article.




### Indexers

| Name | Description |
| --- | --- |
| [``__getitem__(index)``](./__getitem__/#int) | Returns a [ChartSeries](../chartseries/) at the specified index. |

### Properties

| Name | Description |
| --- | --- |
| [count](./count/) | Returns the number of [ChartSeries](../chartseries/) in this collection. |

### Methods

| Name | Description |
| --- | --- |
|[ add(series_name, categories, values)](./add/#str_strlist_floatlist) | Adds new [ChartSeries](../chartseries/) to this collection. Use this method to add series to any type of Bar, Column, Line and Surface charts. |
|[ add(series_name, categories, values, is_subtotal)](./add/#str_strlist_floatlist_boollist) | Adds new [ChartSeries](../chartseries/) to this collection. Use this method to add series to Waterfall charts. |
|[ add_bubbles(series_name, x_values, y_values, bubble_sizes)](./add_bubbles/#str_floatlist_floatlist_floatlist) | Adds new [ChartSeries](../chartseries/) to this collection. Use this method to add series to any type of Bubble charts. |
|[ add_date(series_name, dates, values)](./add_date/#str_datetimelist_floatlist) | Adds new [ChartSeries](../chartseries/) to this collection. Use this method to add series to any type of Area, Radar and Stock charts. |
|[ add_double(series_name, x_values, y_values)](./add_double/#str_floatlist_floatlist) | Adds new [ChartSeries](../chartseries/) to this collection. Use this method to add series to any type of Scatter charts. |
|[ add_double(series_name, x_values)](./add_double/#str_floatlist) | Adds new [ChartSeries](../chartseries/) to this collection. Use this method to add series to Histogram charts. |
|[ add_multilevel_value(series_name, categories, values)](./add_multilevel_value/#str_chartmultilevelvaluelist_floatlist) | Adds new [ChartSeries](../chartseries/) to this collection. Use this method to add series that have multi-level data categories. |
|[ clear()](./clear/#default) | Removes all [ChartSeries](../chartseries/) from this collection. |
|[ remove_at(index)](./remove_at/#int) | Removes a [ChartSeries](../chartseries/) at the specified index. |

### Examples

Shows how to add and remove series data in a chart.

```python
# Inserte un gráfico de columnas que contendrá tres series de datos de demostración por defecto.
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
chart_shape = builder.insert_chart(chart_type=ChartType.COLUMN, width=400, height=300)
chart = chart_shape.chart
chart_data = chart.series
assert chart_data.count == 3
# Imprima el nombre de cada serie en el gráfico.
for series in chart.series:
    print(series.name)
# Estos son los nombres de las categorías en el gráfico.
categories = ['Category 1', 'Category 2', 'Category 3', 'Category 4']
# Podemos agregar una serie con nuevos valores para las categorías existentes.
# Este gráfico ahora contendrá cuatro grupos de cuatro columnas.
chart.series.add(series_name='Series 4', categories=categories, values=[4.4, 7, 3.5, 2.1])
assert chart_data.count == 4
assert chart_data[3].name == 'Series 4'
# Una serie del gráfico también puede ser eliminada por índice, así.
# Esto eliminará una de las tres series de demostración que venían con el gráfico.
chart_data.remove_at(2)
assert not any([s.name == 'Series 3' for s in chart_data])
assert chart_data.count == 3
assert chart_data[2].name == 'Series 4'
# También podemos borrar todos los datos del gráfico de una vez con este método.
# Al crear un nuevo gráfico, esta es la forma de eliminar todos los datos de demostración
# antes de que podamos comenzar a trabajar en un gráfico en blanco.
chart_data.clear()
assert chart_data.count == 0
```

### See Also

* module [aspose.words.drawing.charts](../)

