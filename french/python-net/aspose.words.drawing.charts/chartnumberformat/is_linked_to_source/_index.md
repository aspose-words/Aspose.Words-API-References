---
title: ChartNumberFormat.is_linked_to_source property
linktitle: is_linked_to_source property
articleTitle: is_linked_to_source property
second_title: Aspose.Words for Python
description: "ChartNumberFormat.is_linked_to_source property. Specifies whether the format code is linked to a source cell"
type: docs
weight: 20
url: /fr/python-net/aspose.words.drawing.charts/chartnumberformat/is_linked_to_source/
---

## ChartNumberFormat.is_linked_to_source property

Specifies whether the format code is linked to a source cell.
Default is true.


```python
@property
def is_linked_to_source(self) -> bool:
    ...

@is_linked_to_source.setter
def is_linked_to_source(self, value: bool):
    ...

```

### Remarks

The NumberFormat will be reset to general if format code is linked to source.


### Examples

Shows how to set formatting for chart values.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.COLUMN, width=500, height=300)
chart = shape.chart
# Effacez les séries de données de démonstration du graphique pour commencer avec un graphique vierge.
chart.series.clear()
# Ajoutez une série personnalisée au graphique avec des catégories pour l'axe X,
# et de grandes valeurs numériques respectives pour l'axe Y.
chart.series.add(series_name='Aspose Test Series', categories=['Word', 'PDF', 'Excel', 'GoogleDocs', 'Note'], values=[1900000, 850000, 2100000, 600000, 1500000])
# Définissez le format numérique des libellés des graduations de l'axe Y pour ne pas regrouper les chiffres avec des virgules.
chart.axis_y.number_format.format_code = '#,##0'
# Ce drapeau peut remplacer la valeur ci‑dessus et extraire le format numérique de la cellule source.
self.assertFalse(chart.axis_y.number_format.is_linked_to_source)
doc.save(file_name=ARTIFACTS_DIR + 'Charts.SetNumberFormatToChartAxis.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartNumberFormat](../)

