---
title: Chart class
linktitle: Chart class
articleTitle: Chart class
second_title: Aspose.Words for Python
description: "aspose.words.drawing.charts.Chart class. Provides access to the chart shape properties"
type: docs
weight: 140
url: /it/python-net/aspose.words.drawing.charts/chart/
---

## Chart class

Provides access to the chart shape properties.
To learn more, visit the [Working with Charts](https://docs.aspose.com/words/python-net/working-with-charts/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [axes](./axes/) | Gets a collection of all axes of this chart. |
| [axis_x](./axis_x/) | Provides access to properties of the primary X axis of the chart. |
| [axis_y](./axis_y/) | Provides access to properties of the primary Y axis of the chart. |
| [axis_z](./axis_z/) | Provides access to properties of the Z axis of the chart. |
| [data_table](./data_table/) | Provides access to properties of a data table of this chart. The data table can be shown using the [ChartDataTable.show](../chartdatatable/show/) property. |
| [format](./format/) | Provides access to fill and line formatting of the chart. |
| [legend](./legend/) | Provides access to the chart legend properties. |
| [series](./series/) | Provides access to series collection. |
| [series_groups](./series_groups/) | Provides access to a series group collection of this chart. |
| [source_full_name](./source_full_name/) | Gets the path and name of an xls/xlsx file this chart is linked to. |
| [style](./style/) | Gets or sets the style of the chart. |
| [title](./title/) | Provides access to the chart title properties. |

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

* module [aspose.words.drawing.charts](../)

