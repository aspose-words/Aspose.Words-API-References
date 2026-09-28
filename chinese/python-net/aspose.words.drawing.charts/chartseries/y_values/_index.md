---
title: ChartSeries.y_values property
linktitle: y_values property
articleTitle: y_values property
second_title: Aspose.Words for Python
description: "ChartSeries.y_values property. Gets a collection of Y values for this chart series."
type: docs
weight: 150
url: /zh/python-net/aspose.words.drawing.charts/chartseries/y_values/
---

## ChartSeries.y_values property

Gets a collection of Y values for this chart series.


```python
@property
def y_values(self) -> aspose.words.drawing.charts.ChartYValueCollection:
    ...

```

### Examples

Shows how to work with the format code of the chart data.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 插入一个气泡图表。
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.BUBBLE, width=432, height=252)
chart = shape.chart
# 删除默认生成的系列。
chart.series.clear()
series = chart.series.add_bubbles(series_name='Series1', x_values=[1, 1.9, 2.45, 3], y_values=[1, -0.9, 1.82, 0], bubble_sizes=[2, 1.1, 2.95, 2])
# 显示数据标签。
series.has_data_labels = True
series.data_labels.show_category_name = True
series.data_labels.show_value = True
series.data_labels.show_bubble_size = True
# 设置数据格式代码。
series.x_values.format_code = '#,##0.0#'
series.y_values.format_code = '#,##0.0#;[Red]\\-#,##0.0#'
series.bubble_sizes.format_code = '#,##0.0#'
doc.save(file_name=ARTIFACTS_DIR + 'Charts.FormatCode.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartSeries](../)

