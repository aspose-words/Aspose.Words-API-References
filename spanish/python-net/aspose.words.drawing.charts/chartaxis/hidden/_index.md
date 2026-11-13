---
title: ChartAxis.hidden property
linktitle: hidden property
articleTitle: hidden property
second_title: Aspose.Words for Python
description: "ChartAxis.hidden property. Gets or sets a flag indicating whether this axis is hidden or not."
type: docs
weight: 110
url: /es/python-net/aspose.words.drawing.charts/chartaxis/hidden/
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
# Limpia las series de datos de demostración del gráfico para comenzar con un gráfico limpio.
chart.series.clear()
# Agregar una serie personalizada con categorías para el eje X y valores decimales correspondientes para el eje Y.
chart.series.add(series_name='AW Series 1', categories=['Item 1', 'Item 2', 'Item 3', 'Item 4', 'Item 5'], values=[1.2, 0.3, 2.1, 2.9, 4.2])
# Ocultar los ejes del gráfico para simplificar la apariencia del gráfico.
chart.axis_x.hidden = True
chart.axis_y.hidden = True
doc.save(file_name=ARTIFACTS_DIR + 'Charts.HideChartAxis.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartAxis](../)

