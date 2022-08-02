---
title: text property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets or sets the text of the chart title"
type: docs
weight: 30
url: /python-net/aspose.words.drawing.charts/charttitle/text/
---

## ChartTitle.text property

Gets or sets the text of the chart title.
If null or empty value is specified, auto generated title will be shown.

Use [ChartTitle.show](../show/) option if you need to hide the Title.


### Examples

Shows how to insert a chart and set a title.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Insert a chart shape with a document builder and get its chart.
chart_shape = builder.insert_chart(aw.drawing.charts.ChartType.BAR, 400, 300)
chart = chart_shape.chart

# Use the "title" property to give our chart a title, which appears at the top center of the chart area.
title = chart.title
title.text = "My Chart"

# Set the "show" property to "True" to make the title visible.
title.show = True

# Set the "overlay" property to "True" Give other chart elements more room by allowing them to overlap the title
title.overlay = True

doc.save(ARTIFACTS_DIR + "Charts.chart_title.docx")
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartTitle](../)

