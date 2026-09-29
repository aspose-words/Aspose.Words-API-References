---
title: ChartNumberFormat.is_linked_to_source property
linktitle: is_linked_to_source property
articleTitle: is_linked_to_source property
second_title: Aspose.Words for Python
description: "ChartNumberFormat.is_linked_to_source property. Specifies whether the format code is linked to a source cell"
type: docs
weight: 20
url: /es/python-net/aspose.words.drawing.charts/chartnumberformat/is_linked_to_source/
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
# Limpia las series de datos de demostración del gráfico para comenzar con un gráfico limpio.
chart.series.clear()
# Añade una serie personalizada al gráfico con categorías para el eje X,
# y valores numéricos grandes correspondientes para el eje Y.
chart.series.add(series_name='Aspose Test Series', categories=['Word', 'PDF', 'Excel', 'GoogleDocs', 'Note'], values=[1900000, 850000, 2100000, 600000, 1500000])
# Establece el formato numérico de las etiquetas de marcas del eje Y para que no agrupe los dígitos con comas.
chart.axis_y.number_format.format_code = '#,##0'
# Esta bandera puede sobrescribir el valor anterior y obtener el formato numérico de la celda origen.
self.assertFalse(chart.axis_y.number_format.is_linked_to_source)
doc.save(file_name=ARTIFACTS_DIR + 'Charts.SetNumberFormatToChartAxis.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartNumberFormat](../)

