---
title: AxisScaling.type property
linktitle: type property
articleTitle: type property
second_title: Aspose.Words for Python
description: "AxisScaling.type property. Gets or sets scaling type of the axis."
type: docs
weight: 50
url: /zh/python-net/aspose.words.drawing.charts/axisscaling/type/
---

## AxisScaling.type property

Gets or sets scaling type of the axis.


```python
@property
def type(self) -> aspose.words.drawing.charts.AxisScaleType:
    ...

@type.setter
def type(self, value: aspose.words.drawing.charts.AxisScaleType):
    ...

```

### Remarks

The [AxisScaleType.LINEAR](../../axisscaletype/#LINEAR) value is the only that is allowed in MS Office 2016 new charts.



### Examples

Shows how to apply logarithmic scaling to a chart axis.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
chart_shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.SCATTER, width=450, height=300)
chart = chart_shape.chart
# 清除图表的演示数据系列，以便从空白图表开始。
chart.series.clear()
# 插入一个包含五个点的 X/Y 坐标的系列。
chart.series.add_double(series_name='Series 1', x_values=[1, 2, 3, 4, 5], y_values=[1, 20, 400, 8000, 160000])
# X 轴的刻度默认是线性的，
# 显示均匀递增的值，覆盖我们的 X 值范围 (0, 1, 2, 3...)。
# 线性坐标轴对我们的 Y 值并不理想
# 因为 Y 值较小的点更难读取。
# 以 20 为底的对数刻度 (1, 20, 400, 8000...)
# 会展开绘制的点，使我们更容易在图表上读取它们的数值。
chart.axis_y.scaling.type = aw.drawing.charts.AxisScaleType.LOGARITHMIC
chart.axis_y.scaling.log_base = 20
doc.save(file_name=ARTIFACTS_DIR + 'Charts.AxisScaling.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [AxisScaling](../)

