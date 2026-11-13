---
title: ChartTitle.text property
linktitle: text property
articleTitle: text property
second_title: Aspose.Words for Python
description: "ChartTitle.text property. Gets or sets the text of the chart title"
type: docs
weight: 70
url: /es/python-net/aspose.words.drawing.charts/charttitle/text/
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
# Insertar una forma de gráfico con un document builder y obtener su gráfico.
chart_shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.BAR, width=400, height=300)
chart = chart_shape.chart
# Usar la propiedad "Title" para dar a nuestro gráfico un título, que aparece en la parte superior central del área del gráfico.
title = chart.title
title.text = 'My Chart'
title.font.size = 15
title.font.color = aspose.pydrawing.Color.blue
# Establecer la propiedad "Show" a "true" para hacer visible el título.
title.show = True
# Establecer la propiedad "Overlay" a "true" para dar más espacio a otros elementos del gráfico permitiendo que se superpongan al título
title.overlay = True
doc.save(file_name=ARTIFACTS_DIR + 'Charts.ChartTitle.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartTitle](../)

