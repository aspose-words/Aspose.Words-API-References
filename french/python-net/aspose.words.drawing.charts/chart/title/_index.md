---
title: Chart.title property
linktitle: title property
articleTitle: title property
second_title: Aspose.Words for Python
description: "Chart.title property. Provides access to the chart title properties."
type: docs
weight: 120
url: /fr/python-net/aspose.words.drawing.charts/chart/title/
---

## Chart.title property

Provides access to the chart title properties.


```python
@property
def title(self) -> aspose.words.drawing.charts.ChartTitle:
    ...

```

### Examples

Shows how to insert a chart and set a title.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Insérer une forme de graphique avec un constructeur de document et obtenir son graphique.
chart_shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.BAR, width=400, height=300)
chart = chart_shape.chart
# Utiliser la propriété "Title" pour donner un titre à notre graphique, qui apparaît au centre supérieur de la zone du graphique.
title = chart.title
title.text = 'My Chart'
title.font.size = 15
title.font.color = aspose.pydrawing.Color.blue
# Définir la propriété "Show" sur "true" pour rendre le titre visible.
title.show = True
# Définir la propriété "Overlay" sur "true" Donner plus d'espace aux autres éléments du graphique en leur permettant de chevaucher le titre
title.overlay = True
doc.save(file_name=ARTIFACTS_DIR + 'Charts.ChartTitle.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [Chart](../)

