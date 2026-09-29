---
title: ChartSeriesGroup.series property
linktitle: series property
articleTitle: series property
second_title: Aspose.Words for Python
description: "ChartSeriesGroup.series property. Gets a collection of series that belong to this series group."
type: docs
weight: 100
url: /ru/python-net/aspose.words.drawing.charts/chartseriesgroup/series/
---

## ChartSeriesGroup.series property

Gets a collection of series that belong to this series group.


```python
@property
def series(self) -> aspose.words.drawing.charts.ChartSeriesCollection:
    ...

```

### Examples

Shows how to work with the secondary axis of chart.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.LINE, width=450, height=250)
chart = shape.chart
series = chart.series
# Удалить автоматически сгенерированную серию.
series.clear()
categories = ['Category 1', 'Category 2', 'Category 3']
series.add(series_name='Series 1 of primary series group', categories=categories, values=[2, 3, 4])
series.add(series_name='Series 2 of primary series group', categories=categories, values=[5, 2, 3])
# Создайте дополнительную группу серий, также линейного типа.
new_series_group = chart.series_groups.add(aw.drawing.charts.ChartSeriesType.LINE)
# Укажите использование вторичных осей для новой группы серий.
new_series_group.axis_group = aw.drawing.charts.AxisGroup.SECONDARY
# Скрыть вторичную ось X.
new_series_group.axis_x.hidden = True
# Определите заголовок вторичной оси Y.
new_series_group.axis_y.title.show = True
new_series_group.axis_y.title.text = 'Secondary Y axis'
self.assertEqual(aw.drawing.charts.ChartSeriesType.LINE, new_series_group.series_type)
# Добавьте серию в новую группу серий.
series3 = new_series_group.series.add(series_name='Series of secondary series group', categories=categories, values=[13, 11, 16])
series3.format.stroke.weight = 3.5
doc.save(file_name=ARTIFACTS_DIR + 'Charts.SecondaryAxis.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartSeriesGroup](../)

