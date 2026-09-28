---
title: ChartDataLabelCollection.separator property
linktitle: separator property
articleTitle: separator property
second_title: Aspose.Words for Python
description: "ChartDataLabelCollection.separator property. Gets or sets string separator used for the data labels of the entire series"
type: docs
weight: 90
url: /zh/python-net/aspose.words.drawing.charts/chartdatalabelcollection/separator/
---

## ChartDataLabelCollection.separator property

Gets or sets string separator used for the data labels of the entire series.
The default is a comma, except for pie charts showing only category name and percentage, when a line break
shall be used instead.


```python
@property
def separator(self) -> str:
    ...

@separator.setter
def separator(self, value: str):
    ...

```

### Remarks

Value defined for this property can be overridden for an individual data label with using the
[ChartDataLabel.separator](../../chartdatalabel/separator/) property.



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

Shows how to work with data labels of a pie chart.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
chart = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.PIE, width=500, height=300).chart
# 清除图表的演示数据系列，以便从空白图表开始。
chart.series.clear()
# 插入自定义图表系列，为每个扇区提供类别名称及其频率表。
series = chart.series.add(series_name='Aspose Test Series', categories=['Word', 'PDF', 'Excel'], values=[2.7, 3.2, 0.8])
# 启用数据标签，以显示每个扇区的百分比和频率，并修改其外观。
series.has_data_labels = True
data_labels = series.data_labels
data_labels.show_leader_lines = True
data_labels.show_legend_key = True
data_labels.show_percentage = True
data_labels.show_value = True
data_labels.separator = '; '
doc.save(file_name=ARTIFACTS_DIR + 'Charts.DataLabelsPieChart.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartDataLabelCollection](../)

