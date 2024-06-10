---
title: IChartDataPoint.bubble_3d property
linktitle: bubble_3d property
articleTitle: bubble_3d property
second_title: Aspose.Words for Python
description: "IChartDataPoint.bubble_3d property. Specifies whether the bubbles in Bubble chart should have a 3-D effect applied to them."
type: docs
weight: 10
url: /python-net/aspose.words.drawing.charts/ichartdatapoint/bubble_3d/
---

## IChartDataPoint.bubble_3d property

Specifies whether the bubbles in Bubble chart should have a 3-D effect applied to them.


```python
@property
def bubble_3d(self) -> bool:
    ...

@bubble_3d.setter
def bubble_3d(self, value: bool):
    ...

```

### Examples

Shows how to use 3D effects with bubble charts.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.BUBBLE_3D, width=500, height=350)
chart = shape.chart
self.assertEqual(1, chart.series.count)
self.assertEqual('Y-Values', chart.series[0].name)
self.assertTrue(chart.series[0].bubble_3d)
# Apply a data label to each bubble that displays its diameter.
i = 0
while i < 3:
    chart.series[0].has_data_labels = True
    chart.series[0].data_labels[i].show_bubble_size = True
    chart.series[0].data_labels[i].font.size = 12
    i += 1
doc.save(file_name=ARTIFACTS_DIR + 'Charts.Bubble3D.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [IChartDataPoint](../)

