---
title: AxisScaleType enumeration
linktitle: AxisScaleType enumeration
articleTitle: AxisScaleType enumeration
second_title: Aspose.Words for Python
description: "aspose.words.drawing.charts.AxisScaleType enumeration. Specifies the possible scale types for an axis."
type: docs
weight: 70
url: /es/python-net/aspose.words.drawing.charts/axisscaletype/
---

## AxisScaleType enumeration

Specifies the possible scale types for an axis.


### Members

| Name | Description |
| --- | --- |
| LINEAR | Linear scaling. |
| LOGARITHMIC | Logarithmic scaling. |

### Examples

Shows how to apply logarithmic scaling to a chart axis.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
chart_shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.SCATTER, width=450, height=300)
chart = chart_shape.chart
# Limpia las series de datos de demostración del gráfico para comenzar con un gráfico limpio.
chart.series.clear()
# Inserta una serie con coordenadas X/Y para cinco puntos.
chart.series.add_double(series_name='Series 1', x_values=[1, 2, 3, 4, 5], y_values=[1, 20, 400, 8000, 160000])
# El escalado del eje X es lineal por defecto,
# mostrando valores que incrementan uniformemente y cubren nuestro rango de valores X (0, 1, 2, 3...).
# Un eje lineal no es ideal para nuestros valores Y
# ya que los puntos con los valores Y más pequeños serán más difíciles de leer.
# Una escala logarítmica con una base de 20 (1, 20, 400, 8000...)
# distribuirá los puntos trazados, permitiéndonos leer sus valores en el gráfico más fácilmente.
chart.axis_y.scaling.type = aw.drawing.charts.AxisScaleType.LOGARITHMIC
chart.axis_y.scaling.log_base = 20
doc.save(file_name=ARTIFACTS_DIR + 'Charts.AxisScaling.docx')
```

### See Also

* module [aspose.words.drawing.charts](../)

