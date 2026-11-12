---
title: IChartDataPoint.explosion property
linktitle: explosion property
articleTitle: explosion property
second_title: Aspose.Words for Python
description: "IChartDataPoint.explosion property. Specifies the amount the data point shall be moved from the center of the pie"
type: docs
weight: 20
url: /ru/python-net/aspose.words.drawing.charts/ichartdatapoint/explosion/
---

## IChartDataPoint.explosion property

Specifies the amount the data point shall be moved from the center of the pie.
Can be negative, negative means that property is not set and no explosion should be applied.
Applies only to Pie charts.


```python
@property
def explosion(self) -> int:
    ...

@explosion.setter
def explosion(self, value: int):
    ...

```

### Examples

Shows how to move the slices of a pie chart away from the center.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.PIE, width=500, height=350)
chart = shape.chart
self.assertEqual(1, chart.series.count)
self.assertEqual('Sales', chart.series[0].name)
# "Срезы" круговой диаграммы могут быть отодвинуты от центра на расстояние с помощью атрибута Explosion соответствующей точки данных.
# Добавьте точку данных к первой части круговой диаграммы и отодвиньте её от центра на 10 пунктов.
# Aspose.Words автоматически создает точки данных, если их не существует.
data_point = chart.series[0].data_points[0]
data_point.explosion = 10
# Сместите вторую часть на большее расстояние.
data_point = chart.series[0].data_points[1]
data_point.explosion = 40
doc.save(file_name=ARTIFACTS_DIR + 'Charts.PieChartExplosion.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [IChartDataPoint](../)

