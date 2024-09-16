---
title: Chart class
linktitle: Chart class
articleTitle: Chart class
second_title: Aspose.Words for Python
description: "aspose.words.drawing.charts.Chart class. Provides access to the chart shape properties"
type: docs
weight: 140
url: /python-net/aspose.words.drawing.charts/chart/
---

## Chart class

Provides access to the chart shape properties.
To learn more, visit the [Working with Charts](https://docs.aspose.com/words/python-net/working-with-charts/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [axes](./axes/) | Gets a collection of all axes of this chart. |
| [axis_x](./axis_x/) | Provides access to properties of the primary X axis of the chart. |
| [axis_y](./axis_y/) | Provides access to properties of the primary Y axis of the chart. |
| [axis_z](./axis_z/) | Provides access to properties of the Z axis of the chart. |
| [data_table](./data_table/) | Provides access to properties of a data table of this chart. The data table can be shown using the [ChartDataTable.show](../chartdatatable/show/) property. |
| [format](./format/) | Provides access to fill and line formatting of the chart. |
| [legend](./legend/) | Provides access to the chart legend properties. |
| [series](./series/) | Provides access to series collection. |
| [series_groups](./series_groups/) | Provides access to a series group collection of this chart. |
| [source_full_name](./source_full_name/) | Gets the path and name of an xls/xlsx file this chart is linked to. |
| [title](./title/) | Provides access to the chart title properties. |

### Examples

Shows how to insert a chart and set a title.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Insert a chart shape with a document builder and get its chart.
chart_shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.BAR, width=400, height=300)
chart = chart_shape.chart
# Use the "Title" property to give our chart a title, which appears at the top center of the chart area.
title = chart.title
title.text = 'My Chart'
title.font.size = 15
title.font.color = aspose.pydrawing.Color.blue
# Set the "Show" property to "true" to make the title visible.
title.show = True
# Set the "Overlay" property to "true" Give other chart elements more room by allowing them to overlap the title
title.overlay = True
doc.save(file_name=ARTIFACTS_DIR + 'Charts.ChartTitle.docx')
```

### See Also

* module [aspose.words.drawing.charts](../)

