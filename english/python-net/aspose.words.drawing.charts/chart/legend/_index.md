---
title: Chart.legend property
linktitle: legend property
articleTitle: legend property
second_title: Aspose.Words for Python
description: "Chart.legend property. Provides access to the chart legend properties."
type: docs
weight: 50
url: /python-net/aspose.words.drawing.charts/chart/legend/
---

## Chart.legend property

Provides access to the chart legend properties.


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

* module [aspose.words.drawing.charts](../../)
* class [Chart](../)

