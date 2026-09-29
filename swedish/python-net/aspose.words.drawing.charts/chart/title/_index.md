---
title: Chart.title property
linktitle: title property
articleTitle: title property
second_title: Aspose.Words for Python
description: "Chart.title property. Provides access to the chart title properties."
type: docs
weight: 120
url: /sv/python-net/aspose.words.drawing.charts/chart/title/
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
# Infoga en diagramform med en dokumentbyggare och hämta dess diagram.
chart_shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.BAR, width=400, height=300)
chart = chart_shape.chart
# Använd egenskapen "Title" för att ge vårt diagram en titel, som visas högst upp i mitten av diagramområdet.
title = chart.title
title.text = 'My Chart'
title.font.size = 15
title.font.color = aspose.pydrawing.Color.blue
# Ställ in egenskapen "Show" på "true" för att göra titeln synlig.
title.show = True
# Ställ in egenskapen "Overlay" på "true" Ge andra diagramelement mer utrymme genom att låta dem överlappa titeln
title.overlay = True
doc.save(file_name=ARTIFACTS_DIR + 'Charts.ChartTitle.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [Chart](../)

