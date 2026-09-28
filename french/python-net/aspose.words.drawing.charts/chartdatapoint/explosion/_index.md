---
title: ChartDataPoint.explosion property
linktitle: explosion property
articleTitle: explosion property
second_title: Aspose.Words for Python
description: "ChartDataPoint.explosion property. Specifies the amount the data point shall be moved from the center of the pie"
type: docs
weight: 20
url: /fr/python-net/aspose.words.drawing.charts/chartdatapoint/explosion/
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
# "Tranches" d'un graphique circulaire peuvent être déplacées du centre d'une distance via l'attribut Explosion du point de données correspondant.
# Ajouter un point de données à la première portion du graphique circulaire et le déplacer du centre de 10 points.
# Aspose.Words crée automatiquement des points de données s'ils n'existent pas.
data_point = chart.series[0].data_points[0]
data_point.explosion = 10
# Déplacer la deuxième portion à une distance plus grande.
data_point = chart.series[0].data_points[1]
data_point.explosion = 40
doc.save(file_name=ARTIFACTS_DIR + 'Charts.PieChartExplosion.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartDataPoint](../)

