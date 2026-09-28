---
title: ChartNumberFormat.format_code property
linktitle: format_code property
articleTitle: format_code property
second_title: Aspose.Words for Python
description: "ChartNumberFormat.format_code property. Gets or sets the format code applied to a data label."
type: docs
weight: 10
url: /zh/python-net/aspose.words.drawing.charts/chartnumberformat/format_code/
---

## ChartNumberFormat.format_code property

Gets or sets the format code applied to a data label.


```python
@property
def format_code(self) -> str:
    ...

@format_code.setter
def format_code(self, value: str):
    ...

```

### Remarks

Number formatting is used to change the way a value appears in data label and can be used in some very creative ways.
The examples of number formats:
Number - "#,##0.00"

Currency - "\\"$\\"#,##0.00"

Time - "[$-x-systime]h:mm:ss AM/PM"

Date - "d/mm/yyyy"

Percentage - "0.00%"

Fraction - "# ?/?"

Scientific - "0.00E+00"

Text - "@"

Accounting - "_-\\"$\\"\* #,##0.00_-;-\\"$\\"\* #,##0.00_-;_-\\"$\\"\* \\"-\\"??_-;_-@_-"

Custom with color - "[Red]-#,##0.0"




### Examples

Shows how to enable and configure data labels for a chart series.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 添加折线图，然后清除其演示数据系列，以便从一个干净的图表开始，
# 然后设置标题。
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.LINE, width=500, height=300)
chart = shape.chart
chart.series.clear()
chart.title.text = 'Monthly sales report'
# 插入自定义图表系列，以月份作为 X 轴的类别，
# 以及 Y 轴的相应十进制金额。
series = chart.series.add(series_name='Revenue', categories=['January', 'February', 'March'], values=[25.611, 21.439, 33.75])
# 启用数据标签，然后为显示在数据标签中的值应用自定义数字格式。
# 此格式将把显示的十进制值视为数百万美元。
series.has_data_labels = True
data_labels = series.data_labels
data_labels.show_value = True
data_labels.number_format.format_code = '"US$" #,##0.000"M"'
data_labels.font.size = 12
doc.save(file_name=ARTIFACTS_DIR + 'Charts.DataLabelNumberFormat.docx')
```

Shows how to set formatting for chart values.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.COLUMN, width=500, height=300)
chart = shape.chart
# 清除图表的演示数据系列，以便从空白图表开始。
chart.series.clear()
# 向图表添加一个自定义系列，X 轴使用类别，
# 并为 Y 轴提供相应的大数值。
chart.series.add(series_name='Aspose Test Series', categories=['Word', 'PDF', 'Excel', 'GoogleDocs', 'Note'], values=[1900000, 850000, 2100000, 600000, 1500000])
# 设置 Y 轴刻度标签的数字格式，使其不使用逗号分组数字。
chart.axis_y.number_format.format_code = '#,##0'
# 此标志可以覆盖上述值，并从源单元格获取数字格式。
self.assertFalse(chart.axis_y.number_format.is_linked_to_source)
doc.save(file_name=ARTIFACTS_DIR + 'Charts.SetNumberFormatToChartAxis.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartNumberFormat](../)

