---
title: ChartTitle.overlay property
linktitle: overlay property
articleTitle: overlay property
second_title: Aspose.Words for Python
description: "ChartTitle.overlay property. Determines whether other chart elements shall be allowed to overlap title"
type: docs
weight: 30
url: /python-net/aspose.words.drawing.charts/charttitle/overlay/
---

## ChartTitle.overlay property

Determines whether other chart elements shall be allowed to overlap title.
By default overlay is ``False``.



```python
@property
def overlay(self) -> bool:
    ...

@overlay.setter
def overlay(self, value: bool):
    ...

```

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

* module [aspose.words.drawing.charts](../../)
* class [ChartTitle](../)

