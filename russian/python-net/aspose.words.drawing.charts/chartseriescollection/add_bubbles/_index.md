---
title: ChartSeriesCollection.add_bubbles method
linktitle: add_bubbles method
articleTitle: add_bubbles method
second_title: Aspose.Words for Python
description: "ChartSeriesCollection.add_bubbles method. Adds new [ChartSeries](../../chartseries/) to this collection"
type: docs
weight: 40
url: /ru/python-net/aspose.words.drawing.charts/chartseriescollection/add_bubbles/
---

## add_bubbles(series_name, x_values, y_values, bubble_sizes) {#str_floatlist_floatlist_floatlist}

Adds new [ChartSeries](../../chartseries/) to this collection.
Use this method to add series to any type of Bubble charts.



```python
def add_bubbles(self, series_name: str, x_values: List[float], y_values: List[float], bubble_sizes: List[float]):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| series_name | str |  |
| x_values | List[float] |  |
| y_values | List[float] |  |
| bubble_sizes | List[float] |  |

### Returns

Recently added [ChartSeries](../../chartseries/) object.


### Examples

Shows how to create an appropriate type of chart series for a graph type.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Существует несколько способов заполнения коллекции серий диаграммы.
# Разные схемы серий предназначены для различных типов диаграмм.
# 1 -  Столбчатая диаграмма со столбцами, сгруппированными и объединёнными по оси X по категориям:
chart = ExCharts._append_chart(builder, aw.drawing.charts.ChartType.COLUMN, 500, 300)
categories = ['Category 1', 'Category 2', 'Category 3']
# Вставьте две серии десятичных значений, содержащих значение для каждой соответствующей категории.
# Эта столбчатая диаграмма будет иметь три группы, каждая с двумя столбцами.
chart.series.add(series_name='Series 1', categories=categories, values=[76.6, 82.1, 91.6])
chart.series.add(series_name='Series 2', categories=categories, values=[64.2, 79.5, 94])
# Категории распределены по оси X, а значения — по оси Y.
self.assertEqual(aw.drawing.charts.ChartAxisType.CATEGORY, chart.axis_x.type)
self.assertEqual(aw.drawing.charts.ChartAxisType.VALUE, chart.axis_y.type)
# 2 -  Площадная диаграмма с датами, распределёнными по оси X:
chart = ExCharts._append_chart(builder, aw.drawing.charts.ChartType.AREA, 500, 300)
dates = [datetime.datetime(2014, 3, 31), datetime.datetime(2017, 1, 23), datetime.datetime(2017, 6, 18), datetime.datetime(2019, 11, 22), datetime.datetime(2020, 9, 7)]
# Вставьте серию с десятичным значением для каждой соответствующей даты.
# Даты будут распределены по линейной оси X,
# и добавленные к этой серии значения создадут точки данных.
chart.series.add_date(series_name='Series 1', dates=dates, values=[15.8, 21.5, 22.9, 28.7, 33.1])
self.assertEqual(aw.drawing.charts.ChartAxisType.CATEGORY, chart.axis_x.type)
self.assertEqual(aw.drawing.charts.ChartAxisType.VALUE, chart.axis_y.type)
# 3 -  2D точечный график:
chart = ExCharts._append_chart(builder, aw.drawing.charts.ChartType.SCATTER, 500, 300)
# Каждой серии потребуется два десятичных массива одинаковой длины.
# Первый массив содержит значения X, а второй — соответствующие значения Y
# точек данных на графике диаграммы.
chart.series.add_double(series_name='Series 1', x_values=[3.1, 3.5, 6.3, 4.1, 2.2, 8.3, 1.2, 3.6], y_values=[3.1, 6.3, 4.6, 0.9, 8.5, 4.2, 2.3, 9.9])
chart.series.add_double(series_name='Series 2', x_values=[2.6, 7.3, 4.5, 6.6, 2.1, 9.3, 0.7, 3.3], y_values=[7.1, 6.6, 3.5, 7.8, 7.7, 9.5, 1.3, 4.6])
self.assertEqual(aw.drawing.charts.ChartAxisType.VALUE, chart.axis_x.type)
self.assertEqual(aw.drawing.charts.ChartAxisType.VALUE, chart.axis_y.type)
# 4 -  Диаграмма‑пузырь:
chart = ExCharts._append_chart(builder, aw.drawing.charts.ChartType.BUBBLE, 500, 300)
# Каждой серии потребуется три десятичных массива одинаковой длины.
# Первый массив содержит значения X, второй содержит соответствующие значения Y,
# а третий содержит диаметры для каждой точки данных графика.
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
* class [ChartSeriesCollection](../)

