---
title: ChartLegend class
second_title: Aspose.Words for Python via .NET API Reference
description: "Represents chart legend properties"
type: docs
weight: 190
url: /python-net/aspose.words.drawing.charts/chartlegend/
---

## ChartLegend class

Represents chart legend properties.
To learn more, visit the [Working with Charts](https://docs.aspose.com/words/python-net/working-with-charts/) documentation article.




### Constructors
| Name | Description |
| --- | --- |
| [ChartLegend()](./__init__/#default) | Initializes a new instance of the [ChartLegend](./) class. |

### Properties

| Name | Description |
| --- | --- |
| [legend_entries](./legend_entries/) | Returns a collection of legend entries for all series and trendlines of the parent chart. |
| [overlay](./overlay/) | Determines whether other chart elements shall be allowed to overlap legend. Default value is ``False``. |
| [position](./position/) | Specifies the position of the legend on a chart. Default value is [LegendPosition.RIGHT](../legendposition/#RIGHT). |

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

