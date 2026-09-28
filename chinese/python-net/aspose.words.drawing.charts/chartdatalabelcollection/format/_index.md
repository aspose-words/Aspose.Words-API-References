---
title: ChartDataLabelCollection.format property
linktitle: format property
articleTitle: format property
second_title: Aspose.Words for Python
description: "ChartDataLabelCollection.format property. Provides access to fill and line formatting of the data labels."
type: docs
weight: 40
url: /zh/python-net/aspose.words.drawing.charts/chartdatalabelcollection/format/
---

## ChartDataLabelCollection.format property

Provides access to fill and line formatting of the data labels.


```python
@property
def format(self) -> aspose.words.drawing.charts.ChartFormat:
    ...

```

### Examples

Shows how to set fill, stroke and callout formatting for chart data labels.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.COLUMN, width=432, height=252)
chart = shape.chart
# 删除默认生成的系列。
chart.series.clear()
# 添加新系列。
series = chart.series.add(series_name='AW Series 1', categories=['AW Category 1', 'AW Category 2', 'AW Category 3', 'AW Category 4'], values=[100, 200, 300, 400])
# 显示数据标签。
series.has_data_labels = True
series.data_labels.show_value = True
# 将数据标签格式化为标注框。
format = series.data_labels.format
format.shape_type = aw.drawing.charts.ChartShapeType.WEDGE_RECT_CALLOUT
format.stroke.color = aspose.pydrawing.Color.dark_green
format.fill.solid(aspose.pydrawing.Color.green)
series.data_labels.font.color = aspose.pydrawing.Color.yellow
# 更改单个数据标签的填充和描边。
label_format = series.data_labels[0].format
label_format.stroke.color = aspose.pydrawing.Color.dark_blue
label_format.fill.solid(aspose.pydrawing.Color.blue)
doc.save(file_name=ARTIFACTS_DIR + 'Charts.FormatDataLables.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartDataLabelCollection](../)

