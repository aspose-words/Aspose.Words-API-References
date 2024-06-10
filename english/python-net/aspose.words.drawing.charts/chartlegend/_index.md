---
title: ChartLegend class
linktitle: ChartLegend class
articleTitle: ChartLegend class
second_title: Aspose.Words for Python
description: "aspose.words.drawing.charts.ChartLegend class. Represents chart legend properties"
type: docs
weight: 250
url: /python-net/aspose.words.drawing.charts/chartlegend/
---

## ChartLegend class

Represents chart legend properties.
To learn more, visit the [Working with Charts](https://docs.aspose.com/words/python-net/working-with-charts/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [font](./font/) | Provides access to the default font formatting of legend entries. To override the font formatting for a specific legend entry, use the[ChartLegendEntry.font](../chartlegendentry/font/) property. |
| [format](./format/) | Provides access to fill and line formatting of the legend. |
| [legend_entries](./legend_entries/) | Returns a collection of legend entries for all series and trendlines of the parent chart. |
| [overlay](./overlay/) | Determines whether other chart elements shall be allowed to overlap legend. Default value is ``False``. |
| [position](./position/) | Specifies the position of the legend on a chart. |

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

* module [aspose.words.drawing.charts](../)

