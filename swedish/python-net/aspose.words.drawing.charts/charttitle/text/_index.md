---
title: ChartTitle.text property
linktitle: text property
articleTitle: text property
second_title: Aspose.Words for Python
description: "ChartTitle.text property. Gets or sets the text of the chart title"
type: docs
weight: 70
url: /sv/python-net/aspose.words.drawing.charts/charttitle/text/
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

