---
title: ChartStyle enumeration
linktitle: ChartStyle enumeration
articleTitle: ChartStyle enumeration
second_title: Aspose.Words for Python
description: "aspose.words.drawing.charts.ChartStyle enumeration. Specifies predefined styles of a chart."
type: docs
weight: 390
url: /python-net/aspose.words.drawing.charts/chartstyle/
---

## ChartStyle enumeration

Specifies predefined styles of a chart.


### Members

| Name | Description |
| --- | --- |
| NORMAL | Represents the default chart style. |
| MUTED | A style with muted colors. |
| SATURATED | A style with more saturated colors. |
| SHADED | A style with shaded data points. |
| FLAT | A style with flat data points without gradient. |
| SHADOWED | A style with data points having a shadow. |
| GRADIENT | A style with gradient fill of data points. |
| ORIGINAL | A style with an original appearance of a chart. |
| TRANSPARENT1 | A style with transparent data points. |
| TRANSPARENT2 | A style with transparent data points. |
| OUTLINE | A style with data points having no fill, but only an outline. |
| OUTLINE_BLACK | A style with black chart background, in which data points have no fill, but only an outline. |
| BLACK | A style with black chart background. |
| GREY | A style with gray gradient chart background. |
| BLUE | A style with blue chart background. |
| SHADED_PLOT | A style, in which the plot area is shaded. |

### Examples

Shows how to set and get chart style.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Insert a chart in the Black style.
builder.insert_chart(chart_type=aw.drawing.charts.ChartType.COLUMN, width=400, height=250, chart_style=aw.drawing.charts.ChartStyle.BLACK)
doc.save(file_name=ARTIFACTS_DIR + 'Charts.SetChartStyle.docx')
doc = aw.Document(file_name=ARTIFACTS_DIR + 'Charts.SetChartStyle.docx')
# Get a chart to update.
shape = doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape()
chart = shape.chart
# Get the chart style.
self.assertEqual(aw.drawing.charts.ChartStyle.BLACK, chart.style)
```

### See Also

* module [aspose.words.drawing.charts](../)

