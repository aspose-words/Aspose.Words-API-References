---
title: axis_between_categories property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets or sets a flag indicating whether the value axis crosses the category axis between categories."
type: docs
weight: 10
url: /python-net/aspose.words.drawing.charts/chartaxis/axis_between_categories/
---

## ChartAxis.axis_between_categories property

Gets or sets a flag indicating whether the value axis crosses the category axis between categories.

The property has effect only for value axes. It is not supported by MS Office 2016 new charts.


### Examples

Shows how to get a graph axis to cross at a custom location.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

shape = builder.insert_chart(aw.drawing.charts.ChartType.COLUMN, 450, 250)
chart = shape.chart

self.assertEqual(3, chart.series.count)
self.assertEqual("Series 1", chart.series[0].name)
self.assertEqual("Series 2", chart.series[1].name)
self.assertEqual("Series 3", chart.series[2].name)

# For column charts, the Y-axis crosses at zero by default,
# which means that columns for all values below zero point down to represent negative values.
# We can set a different value for the Y-axis crossing. In this case, we will set it to 3.
axis = chart.axis_x
axis.crosses = aw.drawing.charts.AxisCrosses.CUSTOM
axis.crosses_at = 3
axis.axis_between_categories = True

doc.save(ARTIFACTS_DIR + "Charts.axis_cross.docx")
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartAxis](../)

