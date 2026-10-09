---
title: Chart.plot_area property
linktitle: plot_area property
articleTitle: plot_area property
second_title: Aspose.Words for Python
description: "Chart.plot_area property. Provides access to the plot area properties."
type: docs
weight: 80
url: /python-net/aspose.words.drawing.charts/chart/plot_area/
---

## Chart.plot_area property

Provides access to the plot area properties.


```python
@property
def plot_area(self) -> aspose.words.drawing.charts.ChartPlotArea:
    ...

```

### Examples

Shows how to set fill and line formatting for the plot area of a chart.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.COLUMN, width=432, height=252)
chart = shape.chart
# Delete default generated series and add our own.
series_coll = chart.series
series_coll.clear()
categories = ["Category 1", "Category 2"]
series_coll.add(series_name="Series 1", categories=categories, values=[1, 2])
series_coll.add(series_name="Series 2", categories=categories, values=[3, 4])
# Fill the plot area with a gradient and outline it with a thin blue line.
plot_area = chart.plot_area
plot_area.format.fill.one_color_gradient(color=aspose.pydrawing.Color.light_blue, style=aw.drawing.GradientStyle.DIAGONAL_UP, variant=aw.drawing.GradientVariant.VARIANT2, degree=1)
plot_area.format.stroke.fore_color = aspose.pydrawing.Color.blue
plot_area.format.stroke.weight = 0.25
doc.save(file_name=ARTIFACTS_DIR + "Charts.PlotAreaFormat.docx")
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [Chart](../)

