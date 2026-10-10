---
title: ChartDataLabelCollection.font property
linktitle: font property
articleTitle: font property
second_title: Aspose.Words for Python
description: "ChartDataLabelCollection.font property. Provides access to the font formatting of the data labels of the entire series."
type: docs
weight: 30
url: /zh/python-net/aspose.words.drawing.charts/chartdatalabelcollection/font/
---

## ChartDataLabelCollection.font property

Provides access to the font formatting of the data labels of the entire series.


```python
@property
def font(self) -> aspose.words.Font:
    ...

```

### Remarks

Value defined for this property can be overridden for an individual data label with using the
[ChartDataLabel.font](../../chartdatalabel/font/) property.



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
* class [ChartDataLabelCollection](../)

