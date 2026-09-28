---
title: ChartDataLabelCollection.show_bubble_size property
linktitle: show_bubble_size property
articleTitle: show_bubble_size property
second_title: Aspose.Words for Python
description: "ChartDataLabelCollection.show_bubble_size property. Allows to specify whether bubble size is to be displayed for the data labels of the entire series"
type: docs
weight: 100
url: /zh/python-net/aspose.words.drawing.charts/chartdatalabelcollection/show_bubble_size/
---

## ChartDataLabelCollection.show_bubble_size property

Allows to specify whether bubble size is to be displayed for the data labels of the entire series.
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

### Remarks

Value defined for this property can be overridden for an individual data label with using the
[ChartDataLabel.show_bubble_size](../../chartdatalabel/show_bubble_size/) property.



### Examples

Shows how to work with data labels of a bubble chart.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
chart = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.BUBBLE, width=500, height=300).chart
# 清除图表的演示数据系列，以便从空白图表开始。
chart.series.clear()
# 添加自定义系列，包含每个气泡的 X/Y 坐标和直径。
series = chart.series.add_bubbles(series_name='Aspose Test Series', x_values=[2.9, 3.5, 1.1, 4, 4], y_values=[1.9, 8.5, 2.1, 6, 1.5], bubble_sizes=[9, 4.5, 2.5, 8, 5])
# 启用数据标签，然后修改其外观。
series.has_data_labels = True
data_labels = series.data_labels
data_labels.show_bubble_size = True
data_labels.show_category_name = True
data_labels.show_series_name = True
data_labels.separator = ' & '
doc.save(file_name=ARTIFACTS_DIR + 'Charts.DataLabelsBubbleChart.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartDataLabelCollection](../)

