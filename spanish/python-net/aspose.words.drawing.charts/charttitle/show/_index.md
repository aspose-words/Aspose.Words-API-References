---
title: ChartTitle.show property
linktitle: show property
articleTitle: show property
second_title: Aspose.Words for Python
description: "ChartTitle.show property. Determines whether the title shall be shown for this chart"
type: docs
weight: 60
url: /es/python-net/aspose.words.drawing.charts/charttitle/show/
---

## ChartTitle.show property

Determines whether the title shall be shown for this chart.
Default value is ``True``.



```python
@property
def show(self) -> bool:
    ...

@show.setter
def show(self, value: bool):
    ...

```

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

