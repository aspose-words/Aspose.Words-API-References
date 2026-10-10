---
title: ChartSeriesCollection.count property
linktitle: count property
articleTitle: count property
second_title: Aspose.Words for Python
description: "ChartSeriesCollection.count property. Returns the number of [ChartSeries](../../chartseries/) in this collection."
type: docs
weight: 20
url: /fr/python-net/aspose.words.drawing.charts/chartseriescollection/count/
---

## ChartSeriesCollection.count property

Returns the number of [ChartSeries](../../chartseries/) in this collection.



```python
@property
def count(self) -> int:
    ...

```

### Examples

Shows how to add and remove series data in a chart.

```python
# Insérez un diagramme à colonnes qui contiendra trois séries de données de démonstration par défaut.
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
chart_shape = builder.insert_chart(chart_type=ChartType.COLUMN, width=400, height=300)
chart = chart_shape.chart
chart_data = chart.series
assert chart_data.count == 3
# Affichez le nom de chaque série du diagramme.
for series in chart.series:
    print(series.name)
# Voici les noms des catégories du diagramme.
categories = ['Category 1', 'Category 2', 'Category 3', 'Category 4']
# Nous pouvons ajouter une série avec de nouvelles valeurs pour les catégories existantes.
# Ce diagramme contiendra maintenant quatre groupes de quatre colonnes.
chart.series.add(series_name='Series 4', categories=categories, values=[4.4, 7, 3.5, 2.1])
assert chart_data.count == 4
assert chart_data[3].name == 'Series 4'
# Une série de diagramme peut également être supprimée par indice, comme ceci.
# Cela supprimera l'une des trois séries de démonstration qui accompagnaient le diagramme.
chart_data.remove_at(2)
assert not any([s.name == 'Series 3' for s in chart_data])
assert chart_data.count == 3
assert chart_data[2].name == 'Series 4'
# Nous pouvons également effacer toutes les données du diagramme d'un seul coup avec cette méthode.
# Lors de la création d'un nouveau diagramme, c'est la façon d'effacer toutes les données de démonstration
# avant de pouvoir commencer à travailler sur un diagramme vierge.
chart_data.clear()
assert chart_data.count == 0
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartSeriesCollection](../)

