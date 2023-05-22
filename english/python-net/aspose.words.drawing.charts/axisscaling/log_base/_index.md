---
title: AxisScaling.log_base property
linktitle: log_base property
articleTitle: log_base property
second_title: Aspose.Words for Python
description: "AxisScaling.log_base property. Gets or sets the logarithmic base for a logarithmic axis."
type: docs
weight: 20
url: /python-net/aspose.words.drawing.charts/axisscaling/log_base/
---

## AxisScaling.log_base property

Gets or sets the logarithmic base for a logarithmic axis.

The property is not supported by MS Office 2016 new charts.

Valid range of a floating point value is greater than or equal to 2 and less than or 
equal to 1000. The property has effect only if [AxisScaling.type](../type/) is set to 
[AxisScaleType.LOGARITHMIC](../../axisscaletype/#LOGARITHMIC).

Setting this property sets the [AxisScaling.type](../type/) property to [AxisScaleType.LOGARITHMIC](../../axisscaletype/#LOGARITHMIC).





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
    x_values=[1.0, 2.0, 3.0, 4.0, 5.0],
    y_values=[1.0, 20.0, 400.0, 8000.0, 160000.0])

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

* module [aspose.words.drawing.charts](../../)
* class [AxisScaling](../)

