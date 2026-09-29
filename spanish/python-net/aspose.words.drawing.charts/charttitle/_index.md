---
title: ChartTitle class
linktitle: ChartTitle class
articleTitle: ChartTitle class
second_title: Aspose.Words for Python
description: "aspose.words.drawing.charts.ChartTitle class. Provides access to the chart title properties"
type: docs
weight: 400
url: /es/python-net/aspose.words.drawing.charts/charttitle/
---

## ChartTitle class

Provides access to the chart title properties.
To learn more, visit the [Working with
            Charts](https://docs.aspose.com/words/python-net/working-with-charts/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [font](./font/) | Provides access to the font formatting of the chart title. |
| [format](./format/) | Provides access to fill and line formatting of the chart title. |
| [orientation](./orientation/) | Gets or sets the orientation of the chart title text. |
| [overlay](./overlay/) | Determines whether other chart elements shall be allowed to overlap title. By default overlay is ``False``. |
| [rotation](./rotation/) | Gets or sets the rotation of the chart title in degrees. |
| [show](./show/) | Determines whether the title shall be shown for this chart. Default value is ``True``. |
| [text](./text/) | Gets or sets the text of the chart title. If ``None`` or empty value is specified, auto generated title will be shown. |

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

* module [aspose.words.drawing.charts](../)

