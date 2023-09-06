---
title: LegendPosition enumeration
linktitle: LegendPosition enumeration
articleTitle: LegendPosition enumeration
second_title: Aspose.Words for Python
description: "aspose.words.drawing.charts.LegendPosition enumeration. Specifies the possible positions for a chart legend."
type: docs
weight: 410
url: /python-net/aspose.words.drawing.charts/legendposition/
---

## LegendPosition enumeration

Specifies the possible positions for a chart legend.


### Members

| Name | Description |
| --- | --- |
| NONE | No legend will be shown for the chart. |
| BOTTOM | Specifies that the legend shall be drawn at the bottom of the chart. |
| LEFT | Specifies that the legend shall be drawn at the left of the chart. |
| RIGHT | Specifies that the legend shall be drawn at the right of the chart. |
| TOP | Specifies that the legend shall be drawn at the top of the chart. |
| TOP_RIGHT | Specifies that the legend shall be drawn at the top right of the chart. |

### Examples

Shows how to edit the appearance of a chart's legend.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

shape = builder.insert_chart(aw.drawing.charts.ChartType.LINE, 450, 300)
chart = shape.chart

self.assertEqual(3, chart.series.count)
self.assertEqual("Series 1", chart.series[0].name)
self.assertEqual("Series 2", chart.series[1].name)
self.assertEqual("Series 3", chart.series[2].name)

# Move the chart's legend to the top right corner.
legend = chart.legend
legend.position = aw.drawing.charts.LegendPosition.TOP_RIGHT

# Give other chart elements, such as the graph, more room by allowing them to overlap the legend.
legend.overlay = True

doc.save(ARTIFACTS_DIR + "Charts.chart_legend.docx")
```

### See Also

* module [aspose.words.drawing.charts](../)

