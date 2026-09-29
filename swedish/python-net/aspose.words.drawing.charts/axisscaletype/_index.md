---
title: AxisScaleType enumeration
linktitle: AxisScaleType enumeration
articleTitle: AxisScaleType enumeration
second_title: Aspose.Words for Python
description: "aspose.words.drawing.charts.AxisScaleType enumeration. Specifies the possible scale types for an axis."
type: docs
weight: 70
url: /sv/python-net/aspose.words.drawing.charts/axisscaletype/
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
# Rensa diagrammets demo-dataserier för att börja med ett rent diagram.
chart.series.clear()
# Infoga en serie med X/Y-koordinater för fem punkter.
chart.series.add_double(series_name='Series 1', x_values=[1, 2, 3, 4, 5], y_values=[1, 20, 400, 8000, 160000])
# Skalningen av X-axeln är linjär som standard,
# visar jämnt ökande värden som täcker vårt X-värdesintervall (0, 1, 2, 3...).
# En linjär axel är inte idealisk för våra Y-värden
# eftersom punkterna med de mindre Y-värdena blir svårare att läsa.
# En logaritmisk skalning med basen 20 (1, 20, 400, 8000...)
# kommer att sprida de plottade punkterna, vilket gör att vi kan läsa deras värden på diagrammet lättare.
chart.axis_y.scaling.type = aw.drawing.charts.AxisScaleType.LOGARITHMIC
chart.axis_y.scaling.log_base = 20
doc.save(file_name=ARTIFACTS_DIR + 'Charts.AxisScaling.docx')
```

### See Also

* module [aspose.words.drawing.charts](../)

