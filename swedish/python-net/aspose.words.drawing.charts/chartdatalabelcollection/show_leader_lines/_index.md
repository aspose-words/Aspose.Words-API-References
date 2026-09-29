---
title: ChartDataLabelCollection.show_leader_lines property
linktitle: show_leader_lines property
articleTitle: show_leader_lines property
second_title: Aspose.Words for Python
description: "ChartDataLabelCollection.show_leader_lines property. Allows to specify whether data label leader lines need be shown for the data labels of the entire series"
type: docs
weight: 130
url: /sv/python-net/aspose.words.drawing.charts/chartdatalabelcollection/show_leader_lines/
---

## ChartDataLabelCollection.show_leader_lines property

Allows to specify whether data label leader lines need be shown for the data labels of the entire series.
Default value is ``False``.



```python
@property
def show_leader_lines(self) -> bool:
    ...

@show_leader_lines.setter
def show_leader_lines(self, value: bool):
    ...

```

### Remarks

Applies to Pie charts only.
Leader lines create a visual connection between a data label and its corresponding data point.

Value defined for this property can be overridden for an individual data label with using the
[ChartDataLabel.show_leader_lines](../../chartdatalabel/show_leader_lines/) property.




### Examples

Shows how to work with data labels of a pie chart.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
chart = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.PIE, width=500, height=300).chart
# Rensa diagrammets demo-dataserier för att börja med ett rent diagram.
chart.series.clear()
# Infoga en anpassad diagramserie med ett kategorinamn för varje sektor, och deras frekvenstabell.
series = chart.series.add(series_name='Aspose Test Series', categories=['Word', 'PDF', 'Excel'], values=[2.7, 3.2, 0.8])
# Aktivera datalabels som visar både procent och frekvens för varje sektor, och ändra deras utseende.
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

