---
title: AxisScaling.log_base property
linktitle: log_base property
articleTitle: log_base property
second_title: Aspose.Words for Python
description: "AxisScaling.log_base property. Gets or sets the logarithmic base for a logarithmic axis."
type: docs
weight: 20
url: /zh/python-net/aspose.words.drawing.charts/axisscaling/log_base/
---

## AxisScaling.log_base property

Gets or sets the logarithmic base for a logarithmic axis.


```python
@property
def log_base(self) -> float:
    ...

@log_base.setter
def log_base(self, value: float):
    ...

```

### Remarks

The property is not supported by MS Office 2016 new charts.

Valid range of a floating point value is greater than or equal to 2 and less than or 
equal to 1000. The property has effect only if [AxisScaling.type](../type/) is set to 
[AxisScaleType.LOGARITHMIC](../../axisscaletype/#LOGARITHMIC).

Setting this property sets the [AxisScaling.type](../type/) property to [AxisScaleType.LOGARITHMIC](../../axisscaletype/#LOGARITHMIC).





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

