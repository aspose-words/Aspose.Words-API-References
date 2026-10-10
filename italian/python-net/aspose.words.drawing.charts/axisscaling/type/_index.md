---
title: AxisScaling.type property
linktitle: type property
articleTitle: type property
second_title: Aspose.Words for Python
description: "AxisScaling.type property. Gets or sets scaling type of the axis."
type: docs
weight: 50
url: /it/python-net/aspose.words.drawing.charts/axisscaling/type/
---

## AxisScaling.type property

Gets or sets scaling type of the axis.


```python
@property
def type(self) -> aspose.words.drawing.charts.AxisScaleType:
    ...

@type.setter
def type(self, value: aspose.words.drawing.charts.AxisScaleType):
    ...

```

### Remarks

The [AxisScaleType.LINEAR](../../axisscaletype/#LINEAR) value is the only that is allowed in MS Office 2016 new charts.



### Examples

Shows how to apply logarithmic scaling to a chart axis.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
chart_shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.SCATTER, width=450, height=300)
chart = chart_shape.chart
# Cancella le serie di dati demo del grafico per iniziare con un grafico pulito.
chart.series.clear()
# Inserisci una serie con coordinate X/Y per cinque punti.
chart.series.add_double(series_name='Series 1', x_values=[1, 2, 3, 4, 5], y_values=[1, 20, 400, 8000, 160000])
# La scala dell'asse X è lineare per impostazione predefinita,
# mostrando valori incrementali uniformi che coprono il nostro intervallo di valori X (0, 1, 2, 3...).
# Un asse lineare non è ideale per i nostri valori Y
# poiché i punti con valori Y più piccoli saranno più difficili da leggere.
# Una scala logaritmica con una base di 20 (1, 20, 400, 8000...)
# distribuirà i punti tracciati, consentendoci di leggere i loro valori sul grafico più facilmente.
chart.axis_y.scaling.type = aw.drawing.charts.AxisScaleType.LOGARITHMIC
chart.axis_y.scaling.log_base = 20
doc.save(file_name=ARTIFACTS_DIR + 'Charts.AxisScaling.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [AxisScaling](../)

