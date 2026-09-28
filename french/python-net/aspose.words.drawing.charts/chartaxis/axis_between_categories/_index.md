---
title: ChartAxis.axis_between_categories property
linktitle: axis_between_categories property
articleTitle: axis_between_categories property
second_title: Aspose.Words for Python
description: "ChartAxis.axis_between_categories property. Gets or sets a flag indicating whether the value axis crosses the category axis between categories."
type: docs
weight: 10
url: /fr/python-net/aspose.words.drawing.charts/chartaxis/axis_between_categories/
---

## ChartAxis.axis_between_categories property

Gets or sets a flag indicating whether the value axis crosses the category axis between categories.


```python
@property
def axis_between_categories(self) -> bool:
    ...

@axis_between_categories.setter
def axis_between_categories(self, value: bool):
    ...

```

### Remarks

The property has effect only for value axes. It is not supported by MS Office 2016 new charts.


### Examples

Shows how to get a graph axis to cross at a custom location.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.COLUMN, width=450, height=250)
chart = shape.chart
self.assertEqual(3, chart.series.count)
self.assertEqual('Series 1', chart.series[0].name)
self.assertEqual('Series 2', chart.series[1].name)
self.assertEqual('Series 3', chart.series[2].name)
# Pour les graphiques en colonnes, l'axe Y croise zéro par défaut,
# ce qui signifie que les colonnes pour toutes les valeurs inférieures à zéro pointent vers le bas pour représenter les valeurs négatives.
# Nous pouvons définir une valeur différente pour le croisement de l'axe Y. Dans ce cas, nous le fixerons à 3.
axis = chart.axis_x
axis.crosses = aw.drawing.charts.AxisCrosses.CUSTOM
axis.crosses_at = 3
axis.axis_between_categories = True
doc.save(file_name=ARTIFACTS_DIR + 'Charts.AxisCross.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartAxis](../)

