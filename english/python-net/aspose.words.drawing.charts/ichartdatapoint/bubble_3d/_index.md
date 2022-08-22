﻿---
title: bubble_3d property
second_title: Aspose.Words for Python via .NET API Reference
description: "Specifies whether the bubbles in Bubble chart should have a 3-D effect applied to them."
type: docs
weight: 10
url: /python-net/aspose.words.drawing.charts/ichartdatapoint/bubble_3d/
---

## IChartDataPoint.bubble_3d property

Specifies whether the bubbles in Bubble chart should have a 3-D effect applied to them.


### Examples

Shows how to use 3D effects with bubble charts.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

shape = builder.insert_chart(aw.drawing.charts.ChartType.BUBBLE_3D, 500, 350)
chart = shape.chart

self.assertEqual(1, chart.series.count)
self.assertEqual("Y-Values", chart.series[0].name)
self.assertTrue(chart.series[0].bubble_3d)

# Apply a data label to each bubble that displays its diameter.
for i in range(3):
    chart.series[0].has_data_labels = True
    chart.series[0].data_labels[i].show_bubble_size = True

doc.save(ARTIFACTS_DIR + "Charts.bubble_3d.docx")
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [IChartDataPoint](../)
