---
title: Chart.title property
linktitle: title property
articleTitle: title property
second_title: Aspose.Words for Python
description: "Chart.title property. Provides access to the chart title properties."
type: docs
weight: 110
url: /python-net/aspose.words.drawing.charts/chart/title/
---

## Chart.title property

Provides access to the chart title properties.


```python
@property
def title(self) -> aspose.words.drawing.charts.ChartTitle:
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
* class [Chart](../)

