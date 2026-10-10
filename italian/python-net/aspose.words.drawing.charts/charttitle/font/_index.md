---
title: ChartTitle.font property
linktitle: font property
articleTitle: font property
second_title: Aspose.Words for Python
description: "ChartTitle.font property. Provides access to the font formatting of the chart title."
type: docs
weight: 10
url: /it/python-net/aspose.words.drawing.charts/charttitle/font/
---

## ChartTitle.font property

Provides access to the font formatting of the chart title.


```python
@property
def font(self) -> aspose.words.Font:
    ...

```

### Examples

Shows how to insert a chart and set a title.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Inserisci una forma di grafico con un document builder e ottieni il suo grafico.
chart_shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.BAR, width=400, height=300)
chart = chart_shape.chart
# Usa la proprietà "Title" per dare al nostro grafico un titolo, che appare al centro superiore dell'area del grafico.
title = chart.title
title.text = 'My Chart'
title.font.size = 15
title.font.color = aspose.pydrawing.Color.blue
# Imposta la proprietà "Show" su "true" per rendere il titolo visibile.
title.show = True
# Imposta la proprietà "Overlay" su "true" per dare più spazio agli altri elementi del grafico consentendo loro di sovrapporsi al titolo
title.overlay = True
doc.save(file_name=ARTIFACTS_DIR + 'Charts.ChartTitle.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartTitle](../)

