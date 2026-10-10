---
title: ChartAxis.hidden property
linktitle: hidden property
articleTitle: hidden property
second_title: Aspose.Words for Python
description: "ChartAxis.hidden property. Gets or sets a flag indicating whether this axis is hidden or not."
type: docs
weight: 110
url: /fr/python-net/aspose.words.drawing.charts/chartaxis/hidden/
---

## ChartAxis.hidden property

Gets or sets a flag indicating whether this axis is hidden or not.


```python
@property
def hidden(self) -> bool:
    ...

@hidden.setter
def hidden(self, value: bool):
    ...

```

### Remarks

Default value is ``False``.



### Examples

Shows how to hide chart axes.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.LINE, width=500, height=300)
chart = shape.chart
# Effacez les séries de données de démonstration du graphique pour commencer avec un graphique vierge.
chart.series.clear()
# Ajoutez une série personnalisée avec des catégories pour l'axe X, et des valeurs décimales correspondantes pour l'axe Y.
chart.series.add(series_name='AW Series 1', categories=['Item 1', 'Item 2', 'Item 3', 'Item 4', 'Item 5'], values=[1.2, 0.3, 2.1, 2.9, 4.2])
# Masquez les axes du graphique pour simplifier l'apparence du graphique.
chart.axis_x.hidden = True
chart.axis_y.hidden = True
doc.save(file_name=ARTIFACTS_DIR + 'Charts.HideChartAxis.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartAxis](../)

