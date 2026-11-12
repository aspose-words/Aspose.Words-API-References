---
title: ChartSeriesCollection.remove_at method
linktitle: remove_at method
articleTitle: remove_at method
second_title: Aspose.Words for Python
description: "ChartSeriesCollection.remove_at method. Removes a [ChartSeries](../../chartseries/) at the specified index."
type: docs
weight: 90
url: /ru/python-net/aspose.words.drawing.charts/chartseriescollection/remove_at/
---

## remove_at(index) {#int}

Removes a [ChartSeries](../../chartseries/) at the specified index.



```python
def remove_at(self, index: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | int | The zero-based index of the [ChartSeries](../../chartseries/) to remove. |

### Examples

Shows how to add and remove series data in a chart.

```python
# Вставьте столбчатую диаграмму, которая по умолчанию будет содержать три серии демонстрационных данных.
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
chart_shape = builder.insert_chart(chart_type=ChartType.COLUMN, width=400, height=300)
chart = chart_shape.chart
chart_data = chart.series
assert chart_data.count == 3
# Выведите имя каждой серии в диаграмме.
for series in chart.series:
    print(series.name)
# Это имена категорий в диаграмме.
categories = ['Category 1', 'Category 2', 'Category 3', 'Category 4']
# Мы можем добавить серию с новыми значениями для существующих категорий.
# Эта диаграмма теперь будет содержать четыре кластера по четыре столбца.
chart.series.add(series_name='Series 4', categories=categories, values=[4.4, 7, 3.5, 2.1])
assert chart_data.count == 4
assert chart_data[3].name == 'Series 4'
# Серию диаграммы также можно удалить по индексу, как показано.
# Это удалит одну из трёх демонстрационных серий, поставляемых с диаграммой.
chart_data.remove_at(2)
assert not any([s.name == 'Series 3' for s in chart_data])
assert chart_data.count == 3
assert chart_data[2].name == 'Series 4'
# Мы также можем очистить все данные диаграммы сразу с помощью этого метода.
# При создании новой диаграммы это способ удалить все демонстрационные данные
# прежде чем мы сможем начать работу с пустой диаграммой.
chart_data.clear()
assert chart_data.count == 0
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartSeriesCollection](../)

