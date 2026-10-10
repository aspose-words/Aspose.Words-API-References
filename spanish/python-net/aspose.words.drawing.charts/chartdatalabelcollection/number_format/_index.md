---
title: ChartDataLabelCollection.number_format property
linktitle: number_format property
articleTitle: number_format property
second_title: Aspose.Words for Python
description: "ChartDataLabelCollection.number_format property. Gets an [ChartNumberFormat](../../chartnumberformat/) instance allowing to set number format for the data labels of the entire series."
type: docs
weight: 50
url: /es/python-net/aspose.words.drawing.charts/chartdatalabelcollection/number_format/
---

## ChartDataLabelCollection.number_format property

Gets an [ChartNumberFormat](../../chartnumberformat/) instance allowing to set number format for the data labels of the
entire series.



```python
@property
def number_format(self) -> aspose.words.drawing.charts.ChartNumberFormat:
    ...

```

### Examples

Shows how to enable and configure data labels for a chart series.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Agregar un gráfico de líneas, luego borrar su serie de datos de demostración para comenzar con un gráfico limpio,
# y luego establecer un título.
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.LINE, width=500, height=300)
chart = shape.chart
chart.series.clear()
chart.title.text = 'Monthly sales report'
# Insertar una serie de gráfico personalizada con los meses como categorías para el eje X,
# y cantidades decimales respectivas para el eje Y.
series = chart.series.add(series_name='Revenue', categories=['January', 'February', 'March'], values=[25.611, 21.439, 33.75])
# Habilitar etiquetas de datos y luego aplicar un formato numérico personalizado para los valores mostrados en las etiquetas de datos.
# Este formato tratará los valores decimales mostrados como millones de dólares estadounidenses.
series.has_data_labels = True
data_labels = series.data_labels
data_labels.show_value = True
data_labels.number_format.format_code = '"US$" #,##0.000"M"'
data_labels.font.size = 12
doc.save(file_name=ARTIFACTS_DIR + 'Charts.DataLabelNumberFormat.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartDataLabelCollection](../)

