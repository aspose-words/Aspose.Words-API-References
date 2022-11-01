---
title: AxisScaling class
second_title: Aspose.Words for Python via .NET API Reference
description: "Represents the scaling options of the axis"
type: docs
weight: 70
url: /python-net/aspose.words.drawing.charts/axisscaling/
---

## AxisScaling class

Represents the scaling options of the axis.
To learn more, visit the [Working with Charts](https://docs.aspose.com/words/net/working-with-charts/) documentation article.




### Constructors
| Name | Description |
| --- | --- |
| [AxisScaling()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [log_base](./log_base/) | Gets or sets the logarithmic base for a logarithmic axis. |
| [maximum](./maximum/) | Gets or sets the maximum value of the axis. |
| [minimum](./minimum/) | Gets or sets minimum value of the axis. |
| [type](./type/) | Gets or sets scaling type of the axis. |

### Examples

Shows how to apply logarithmic scaling to a chart axis.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

chart_shape = builder.insert_chart(aw.drawing.charts.ChartType.SCATTER, 450, 300)
chart = chart_shape.chart

# Clear the chart's demo data series to start with a clean chart.
chart.series.clear()

# Insert a series with X/Y coordinates for five points.
chart.series.add("Series 1",
    [1.0, 2.0, 3.0, 4.0, 5.0],
    [1.0, 20.0, 400.0, 8000.0, 160000.0])

# The scaling of the X-axis is linear by default,
# displaying evenly incrementing values that cover our X-value range (0, 1, 2, 3...).
# A linear axis is not ideal for our Y-values
# since the points with the smaller Y-values will be harder to read.
# A logarithmic scaling with a base of 20 (1, 20, 400, 8000...)
# will spread the plotted points, allowing us to read their values on the chart more easily.
chart.axis_y.scaling.type = aw.drawing.charts.AxisScaleType.LOGARITHMIC
chart.axis_y.scaling.log_base = 20

doc.save(ARTIFACTS_DIR + "Charts.axis_scaling.docx")
```

### See Also

* module [aspose.words.drawing.charts](../)

