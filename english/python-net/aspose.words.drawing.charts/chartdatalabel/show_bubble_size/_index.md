---
title: ChartDataLabel.show_bubble_size property
linktitle: show_bubble_size property
articleTitle: show_bubble_size property
second_title: Aspose.Words for Python
description: "ChartDataLabel.show_bubble_size property. Allows to specify if bubble size is to be displayed for the data labels on a chart"
type: docs
weight: 80
url: /python-net/aspose.words.drawing.charts/chartdatalabel/show_bubble_size/
---

## ChartDataLabel.show_bubble_size property

Allows to specify if bubble size is to be displayed for the data labels on a chart. 
Applies only to Bubble charts. 
Default value is ``False``.



```python
@property
def show_bubble_size(self) -> bool:
    ...

@show_bubble_size.setter
def show_bubble_size(self, value: bool):
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
* class [ChartDataLabel](../)

