---
title: ChartTitle class
linktitle: ChartTitle class
articleTitle: ChartTitle class
second_title: Aspose.Words for Python
description: "aspose.words.drawing.charts.ChartTitle class. Provides access to the chart title properties"
type: docs
weight: 390
url: /python-net/aspose.words.drawing.charts/charttitle/
---

## ChartTitle class

Provides access to the chart title properties.
To learn more, visit the [Working with
            Charts](https://docs.aspose.com/words/python-net/working-with-charts/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [font](./font/) | Provides access to the font formatting of the chart title. |
| [format](./format/) | Provides access to fill and line formatting of the chart title. |
| [overlay](./overlay/) | Determines whether other chart elements shall be allowed to overlap title. By default overlay is ``False``. |
| [show](./show/) | Determines whether the title shall be shown for this chart. Default value is ``True``. |
| [text](./text/) | Gets or sets the text of the chart title. If ``None`` or empty value is specified, auto generated title will be shown. |

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

