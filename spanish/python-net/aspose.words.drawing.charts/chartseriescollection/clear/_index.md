---
title: ChartSeriesCollection.clear method
linktitle: clear method
articleTitle: clear method
second_title: Aspose.Words for Python
description: "ChartSeriesCollection.clear method. Removes all [ChartSeries](../../chartseries/) from this collection."
type: docs
weight: 80
url: /es/python-net/aspose.words.drawing.charts/chartseriescollection/clear/
---

## clear() {#default}

Removes all [ChartSeries](../../chartseries/) from this collection.



```python
def clear(self):
    ...
```

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

* module [aspose.words.drawing.charts](../../)
* class [ChartSeriesCollection](../)

