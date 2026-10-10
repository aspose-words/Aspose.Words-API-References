---
title: AxisScaling class
linktitle: AxisScaling class
articleTitle: AxisScaling class
second_title: Aspose.Words for Python
description: "aspose.words.drawing.charts.AxisScaling class. Represents the scaling options of the axis"
type: docs
weight: 80
url: /de/python-net/aspose.words.drawing.charts/axisscaling/
---

## AxisScaling class

Represents the scaling options of the axis.
To learn more, visit the [Working with Charts](https://docs.aspose.com/words/python-net/working-with-charts/) documentation article.




### Constructors
| Name | Description |
| --- | --- |
| [AxisScaling()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [log_base](./log_base/) | Gets or sets the logarithmic base for a logarithmic axis. |
| [maximum](./maximum/) | Gets or sets the maximum value of the axis. |
| [minimum](./minimum/) | Gets or sets minimum value of the axis. |
| [type](./type/) | Gets or sets scaling type of the axis. |

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

