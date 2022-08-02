---
title: explosion property
second_title: Aspose.Words for Python via .NET API Reference
description: "Specifies the amount the data point shall be moved from the center of the pie"
type: docs
weight: 20
url: /python-net/aspose.words.drawing.charts/ichartdatapoint/explosion/
---

## IChartDataPoint.explosion property

Specifies the amount the data point shall be moved from the center of the pie.
Can be negative, negative means that property is not set and no explosion should be applied.
Applies only to Pie charts.


### Examples

Shows how to move the slices of a pie chart away from the center.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

shape = builder.insert_chart(aw.drawing.charts.ChartType.PIE, 500, 350)
chart = shape.chart

self.assertEqual(1, chart.series.count)
self.assertEqual("Sales", chart.series[0].name)

# "Slices" of a pie chart may be moved away from the center by a distance via the respective data point's Explosion attribute.
# Add a data point to the first portion of the pie chart and move it away from the center by 10 points.
# Aspose.Words create data points automatically if them does not exist.
data_point = chart.series[0].data_points[0]
data_point.explosion = 10

# Displace the second portion by a greater distance.
data_point = chart.series[0].data_points[1]
data_point.explosion = 40

doc.save(ARTIFACTS_DIR + "Charts.pie_chart_explosion.docx")
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [IChartDataPoint](../)

