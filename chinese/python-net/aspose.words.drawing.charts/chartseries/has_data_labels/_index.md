---
title: ChartSeries.has_data_labels property
linktitle: has_data_labels property
articleTitle: has_data_labels property
second_title: Aspose.Words for Python
description: "ChartSeries.has_data_labels property. Gets or sets a flag indicating whether data labels are displayed for the series."
type: docs
weight: 70
url: /zh/python-net/aspose.words.drawing.charts/chartseries/has_data_labels/
---

## ChartSeries.has_data_labels property

Gets or sets a flag indicating whether data labels are displayed for the series.


```python
@property
def has_data_labels(self) -> bool:
    ...

@has_data_labels.setter
def has_data_labels(self, value: bool):
    ...

```

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

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartSeries](../)

