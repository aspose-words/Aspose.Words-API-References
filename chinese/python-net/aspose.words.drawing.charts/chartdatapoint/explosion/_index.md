---
title: ChartDataPoint.explosion property
linktitle: explosion property
articleTitle: explosion property
second_title: Aspose.Words for Python
description: "ChartDataPoint.explosion property. Specifies the amount the data point shall be moved from the center of the pie"
type: docs
weight: 20
url: /zh/python-net/aspose.words.drawing.charts/chartdatapoint/explosion/
---

## ChartDataPoint.explosion property

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
# 饼图的"Slices"可以通过相应数据点的 Explosion 属性，以一定距离从中心移开。
# 向饼图的第一部分添加一个数据点，并将其向中心外移动 10 个点。
# 如果不存在，Aspose.Words 会自动创建数据点。
data_point = chart.series[0].data_points[0]
data_point.explosion = 10
# 将第二部分以更大的距离位移。
data_point = chart.series[0].data_points[1]
data_point.explosion = 40
doc.save(file_name=ARTIFACTS_DIR + 'Charts.PieChartExplosion.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartDataPoint](../)

