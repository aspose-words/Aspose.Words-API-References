---
title: ChartLegendEntry class
linktitle: ChartLegendEntry class
articleTitle: ChartLegendEntry class
second_title: Aspose.Words for Python
description: "aspose.words.drawing.charts.ChartLegendEntry class. Represents a chart legend entry"
type: docs
weight: 280
url: /python-net/aspose.words.drawing.charts/chartlegendentry/
---

## ChartLegendEntry class

Represents a chart legend entry.
To learn more, visit the [Working with Charts](https://docs.aspose.com/words/python-net/working-with-charts/) documentation article.




### Remarks

A legend entry corresponds to a specific chart series or trendline.

The text of the entry is the name of the series or trendline. The text cannot be changed.




### Properties

| Name | Description |
| --- | --- |
| [font](./font/) | Provides access to the font formatting of this legend entry. |
| [is_hidden](./is_hidden/) | Gets or sets a value indicating whether this entry is hidden in the chart legend. The default value is **false**. |

### Examples

Shows how to work with a legend font.

```python
doc = aw.Document(file_name=MY_DIR + 'Reporting engine template - Chart series.docx')
chart = doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape().chart
chart_legend = chart.legend
# Set default font size all legend entries.
chart_legend.font.size = 14
# Change font for specific legend entry.
chart_legend.legend_entries[1].font.italic = True
chart_legend.legend_entries[1].font.size = 12
# Get legend entry for chart series.
legend_entry = chart.series[0].legend_entry
doc.save(file_name=ARTIFACTS_DIR + 'Charts.LegendFont.docx')
```

### See Also

* module [aspose.words.drawing.charts](../)
* property [ChartSeries.legend_entry](../chartseries/legend_entry/)

