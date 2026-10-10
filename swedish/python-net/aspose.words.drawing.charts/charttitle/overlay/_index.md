---
title: ChartTitle.overlay property
linktitle: overlay property
articleTitle: overlay property
second_title: Aspose.Words for Python
description: "ChartTitle.overlay property. Determines whether other chart elements shall be allowed to overlap title"
type: docs
weight: 40
url: /sv/python-net/aspose.words.drawing.charts/charttitle/overlay/
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
* class [ChartTitle](../)

