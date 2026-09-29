---
title: ChartDataLabelCollection.show_percentage property
linktitle: show_percentage property
articleTitle: show_percentage property
second_title: Aspose.Words for Python
description: "ChartDataLabelCollection.show_percentage property. Allows to specify whether percentage value is to be displayed for the data labels of the entire series"
type: docs
weight: 150
url: /es/python-net/aspose.words.drawing.charts/chartdatalabelcollection/show_percentage/
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
# Limpia las series de datos de demostración del gráfico para comenzar con un gráfico limpio.
chart.series.clear()
# Insertar una serie de gráfico personalizada con un nombre de categoría para cada uno de los sectores y su tabla de frecuencias.
series = chart.series.add(series_name='Aspose Test Series', categories=['Word', 'PDF', 'Excel'], values=[2.7, 3.2, 0.8])
# Habilitar etiquetas de datos que mostrarán tanto el porcentaje como la frecuencia de cada sector y modificar su apariencia.
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

