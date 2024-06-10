---
title: Chart.legend property
linktitle: legend property
articleTitle: legend property
second_title: Aspose.Words for Python
description: "Chart.legend property. Provides access to the chart legend properties."
type: docs
weight: 70
url: /python-net/aspose.words.drawing.charts/chart/legend/
---

## Chart.legend property

Provides access to the chart legend properties.


```python
@property
def legend(self) -> aspose.words.drawing.charts.ChartLegend:
    ...

```

### Examples

Shows how to edit the appearance of a chart's legend.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.LINE, width=450, height=300)
chart = shape.chart
self.assertEqual(3, chart.series.count)
self.assertEqual('Series 1', chart.series[0].name)
self.assertEqual('Series 2', chart.series[1].name)
self.assertEqual('Series 3', chart.series[2].name)
# Move the chart's legend to the top right corner.
legend = chart.legend
legend.position = aw.drawing.charts.LegendPosition.TOP_RIGHT
# Give other chart elements, such as the graph, more room by allowing them to overlap the legend.
legend.overlay = True
doc.save(file_name=ARTIFACTS_DIR + 'Charts.ChartLegend.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [Chart](../)

