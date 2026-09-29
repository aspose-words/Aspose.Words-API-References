---
title: IChartDataPoint.explosion property
linktitle: explosion property
articleTitle: explosion property
second_title: Aspose.Words for Python
description: "IChartDataPoint.explosion property. Specifies the amount the data point shall be moved from the center of the pie"
type: docs
weight: 20
url: /tr/python-net/aspose.words.drawing.charts/ichartdatapoint/explosion/
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
# \"Dilimler\" bir pasta grafiğinde, ilgili veri noktasının Explosion özelliği ile merkezden bir mesafe kadar uzaklaştırılabilir.
# Pasta grafiğinin ilk dilimine bir veri noktası ekleyin ve onu merkezden 10 birim uzaklaştırın.
# Aspose.Words veri noktaları mevcut değilse otomatik olarak oluşturur.
data_point = chart.series[0].data_points[0]
data_point.explosion = 10
# İkinci dilimi daha büyük bir mesafe kadar kaydırın.
data_point = chart.series[0].data_points[1]
data_point.explosion = 40
doc.save(file_name=ARTIFACTS_DIR + 'Charts.PieChartExplosion.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [IChartDataPoint](../)

