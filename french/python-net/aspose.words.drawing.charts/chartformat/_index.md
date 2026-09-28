---
title: ChartFormat class
linktitle: ChartFormat class
articleTitle: ChartFormat class
second_title: Aspose.Words for Python
description: "aspose.words.drawing.charts.ChartFormat class. Represents the formatting of a chart element"
type: docs
weight: 260
url: /fr/python-net/aspose.words.drawing.charts/chartformat/
---

## ChartFormat class

Represents the formatting of a chart element.
To learn more, visit the [Working with Charts](https://docs.aspose.com/words/python-net/working-with-charts/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [fill](./fill/) | Gets fill formatting for the parent chart element. |
| [is_defined](./is_defined/) | Gets a flag indicating whether any format is defined. |
| [shape_type](./shape_type/) | Gets or sets the shape type of the parent chart element. |
| [stroke](./stroke/) | Gets line formatting for the parent chart element. |

### Methods

| Name | Description |
| --- | --- |
|[ set_default_fill()](./set_default_fill/#default) | Resets the fill of the chart element to have the default value. |

### Examples

Shows how to use chart formating.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.COLUMN, width=432, height=252)
chart = shape.chart
# Supprimez les séries générées par défaut.
series = chart.series
series.clear()
categories = ['Category 1', 'Category 2']
series.add(series_name='Series 1', categories=categories, values=[1, 2])
series.add(series_name='Series 2', categories=categories, values=[3, 4])
# Formatez l'arrière-plan du graphique.
chart.format.fill.solid(aspose.pydrawing.Color.dark_slate_gray)
# Masquez les libellés des graduations d'axe.
chart.axis_x.tick_labels.position = aw.drawing.charts.AxisTickLabelPosition.NONE
chart.axis_y.tick_labels.position = aw.drawing.charts.AxisTickLabelPosition.NONE
# Formatez le titre du graphique.
chart.title.format.fill.solid(aspose.pydrawing.Color.light_goldenrod_yellow)
# Formatez le titre de l'axe.
chart.axis_x.title.show = True
chart.axis_x.title.format.fill.solid(aspose.pydrawing.Color.light_goldenrod_yellow)
# Formatez la légende.
chart.legend.format.fill.solid(aspose.pydrawing.Color.light_goldenrod_yellow)
doc.save(file_name=ARTIFACTS_DIR + 'Charts.ChartFormat.docx')
```

### See Also

* module [aspose.words.drawing.charts](../)

