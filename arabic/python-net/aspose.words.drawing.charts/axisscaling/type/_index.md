---
title: AxisScaling.type property
linktitle: type property
articleTitle: type property
second_title: Aspose.Words for Python
description: "AxisScaling.type property. Gets or sets scaling type of the axis."
type: docs
weight: 50
url: /ar/python-net/aspose.words.drawing.charts/axisscaling/type/
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
# مسح سلسلة بيانات العرض التجريبية للمخطط للبدء بمخطط نظيف.
chart.series.clear()
# إدراج سلسلة بإحداثيات X/Y لخمسة نقاط.
chart.series.add_double(series_name='Series 1', x_values=[1, 2, 3, 4, 5], y_values=[1, 20, 400, 8000, 160000])
# تحجيم المحور X خطي افتراضياً،
# مع عرض قيم تتزايد بالتساوي تغطي نطاق قيم X لدينا (0، 1، 2، 3...).
# A linear axis is not ideal for our Y-values
# since the points with the smaller Y-values will be harder to read.
# A logarithmic scaling with a base of 20 (1, 20, 400, 8000...)
# will spread the plotted points, allowing us to read their values on the chart more easily.
chart.axis_y.scaling.type = aw.drawing.charts.AxisScaleType.LOGARITHMIC
chart.axis_y.scaling.log_base = 20
doc.save(file_name=ARTIFACTS_DIR + 'Charts.AxisScaling.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [AxisScaling](../)

