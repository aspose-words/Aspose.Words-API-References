---
title: ChartTitle.text property
linktitle: text property
articleTitle: text property
second_title: Aspose.Words for Python
description: "ChartTitle.text property. Gets or sets the text of the chart title"
type: docs
weight: 40
url: /python-net/aspose.words.drawing.charts/charttitle/text/
---

## ChartTitle.text property

Gets or sets the text of the chart title.
If ``None`` or empty value is specified, auto generated title will be shown.



```python
@property
def text(self) -> str:
    ...

@text.setter
def text(self, value: str):
    ...

```

### Remarks

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
title.font.size = 15
title.font.color = drawing.Color.blue

# Set the "show" property to "True" to make the title visible.
title.show = True

# Set the "overlay" property to "True" Give other chart elements more room by allowing them to overlap the title
title.overlay = True

doc.save(ARTIFACTS_DIR + "Charts.chart_title.docx")
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartTitle](../)

