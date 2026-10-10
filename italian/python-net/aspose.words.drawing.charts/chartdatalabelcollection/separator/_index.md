---
title: ChartDataLabelCollection.separator property
linktitle: separator property
articleTitle: separator property
second_title: Aspose.Words for Python
description: "ChartDataLabelCollection.separator property. Gets or sets string separator used for the data labels of the entire series"
type: docs
weight: 90
url: /it/python-net/aspose.words.drawing.charts/chartdatalabelcollection/separator/
---

## ChartDataLabelCollection.separator property

Gets or sets string separator used for the data labels of the entire series.
The default is a comma, except for pie charts showing only category name and percentage, when a line break
shall be used instead.


```python
@property
def separator(self) -> str:
    ...

@separator.setter
def separator(self, value: str):
    ...

```

### Remarks

Value defined for this property can be overridden for an individual data label with using the
[ChartDataLabel.separator](../../chartdatalabel/separator/) property.



### Examples

Shows how to work with data labels of a bubble chart.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
chart = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.BUBBLE, width=500, height=300).chart
# Cancella le serie di dati demo del grafico per iniziare con un grafico pulito.
chart.series.clear()
# Aggiungi una serie personalizzata con coordinate X/Y e diametro di ciascuna bolla.
series = chart.series.add_bubbles(series_name='Aspose Test Series', x_values=[2.9, 3.5, 1.1, 4, 4], y_values=[1.9, 8.5, 2.1, 6, 1.5], bubble_sizes=[9, 4.5, 2.5, 8, 5])
# Abilita le etichette dei dati, quindi modifica il loro aspetto.
series.has_data_labels = True
data_labels = series.data_labels
data_labels.show_bubble_size = True
data_labels.show_category_name = True
data_labels.show_series_name = True
data_labels.separator = ' & '
doc.save(file_name=ARTIFACTS_DIR + 'Charts.DataLabelsBubbleChart.docx')
```

Shows how to work with data labels of a pie chart.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
chart = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.PIE, width=500, height=300).chart
# Cancella le serie di dati demo del grafico per iniziare con un grafico pulito.
chart.series.clear()
# Inserisci una serie di grafico personalizzata con un nome di categoria per ciascuno dei settori e la loro tabella di frequenza.
series = chart.series.add(series_name='Aspose Test Series', categories=['Word', 'PDF', 'Excel'], values=[2.7, 3.2, 0.8])
# Abilita le etichette dei dati che mostreranno sia la percentuale che la frequenza di ciascun settore e modifica il loro aspetto.
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

