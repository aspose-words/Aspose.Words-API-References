---
title: AxisScaleType enumeration
linktitle: AxisScaleType enumeration
articleTitle: AxisScaleType enumeration
second_title: Aspose.Words for Python
description: "aspose.words.drawing.charts.AxisScaleType enumeration. Specifies the possible scale types for an axis."
type: docs
weight: 70
url: /de/python-net/aspose.words.drawing.charts/axisscaletype/
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
# Leeren Sie die Demo‑Datenserien des Diagramms, um mit einem leeren Diagramm zu beginnen.
chart.series.clear()
# Fügen Sie eine Serie mit X/Y‑Koordinaten für fünf Punkte ein.
chart.series.add_double(series_name='Series 1', x_values=[1, 2, 3, 4, 5], y_values=[1, 20, 400, 8000, 160000])
# Die Skalierung der X‑Achse ist standardmäßig linear,
# zeigt gleichmäßig steigende Werte, die unseren X‑Wertbereich (0, 1, 2, 3…) abdecken.
# Eine lineare Achse ist für unsere Y-Werte nicht ideal
# da die Punkte mit den kleineren Y-Werten schwerer zu lesen sein werden.
# Eine logarithmische Skalierung mit einer Basis von 20 (1, 20, 400, 8000...)
# verteilt die geplotteten Punkte, sodass wir ihre Werte im Diagramm leichter ablesen können.
chart.axis_y.scaling.type = aw.drawing.charts.AxisScaleType.LOGARITHMIC
chart.axis_y.scaling.log_base = 20
doc.save(file_name=ARTIFACTS_DIR + 'Charts.AxisScaling.docx')
```

### See Also

* module [aspose.words.drawing.charts](../)

