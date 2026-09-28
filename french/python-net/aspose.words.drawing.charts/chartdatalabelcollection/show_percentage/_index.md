---
title: ChartDataLabelCollection.show_percentage property
linktitle: show_percentage property
articleTitle: show_percentage property
second_title: Aspose.Words for Python
description: "ChartDataLabelCollection.show_percentage property. Allows to specify whether percentage value is to be displayed for the data labels of the entire series"
type: docs
weight: 150
url: /fr/python-net/aspose.words.drawing.charts/chartdatalabelcollection/show_percentage/
---

## ChartDataLabelCollection.show_percentage property

Allows to specify whether percentage value is to be displayed for the data labels of the entire series.
Default value is ``False``. Applies only to Pie charts.



```python
@property
def show_percentage(self) -> bool:
    ...

@show_percentage.setter
def show_percentage(self, value: bool):
    ...

```

### Remarks

Value defined for this property can be overridden for an individual data label with using the
[ChartDataLabel.show_percentage](../../chartdatalabel/show_percentage/) property.



### Examples

Shows how to work with data labels of a pie chart.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
chart = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.PIE, width=500, height=300).chart
# Effacez les séries de données de démonstration du graphique pour commencer avec un graphique vierge.
chart.series.clear()
# Insérer une série de graphique personnalisée avec un nom de catégorie pour chaque secteur, ainsi que leur tableau de fréquences.
series = chart.series.add(series_name='Aspose Test Series', categories=['Word', 'PDF', 'Excel'], values=[2.7, 3.2, 0.8])
# Activer les étiquettes de données qui afficheront à la fois le pourcentage et la fréquence de chaque secteur, et modifier leur apparence.
series.has_data_labels = True
data_labels = series.data_labels
data_labels.show_leader_lines = True
data_labels.show_legend_key = True
data_labels.show_percentage = True
data_labels.show_value = True
data_labels.separator = '; '
doc.save(file_name=ARTIFACTS_DIR + 'Charts.DataLabelsPieChart.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartDataLabelCollection](../)

