---
title: AxisScaling.log_base property
linktitle: log_base property
articleTitle: log_base property
second_title: Aspose.Words for Python
description: "AxisScaling.log_base property. Gets or sets the logarithmic base for a logarithmic axis."
type: docs
weight: 20
url: /tr/python-net/aspose.words.drawing.charts/axisscaling/log_base/
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
# Temiz bir grafikle başlamak için grafiğin demo veri serilerini temizleyin.
chart.series.clear()
# Beş nokta için X/Y koordinatları içeren bir seri ekleyin.
chart.series.add_double(series_name='Series 1', x_values=[1, 2, 3, 4, 5], y_values=[1, 20, 400, 8000, 160000])
# X-ekseninin ölçeklendirmesi varsayılan olarak doğrusaldır,
# (0, 1, 2, 3...). gibi X-değeri aralığımızı kapsayan eşit artan değerleri gösterir.
# Doğrusal bir eksen, Y-değerlerimiz için ideal değildir
# çünkü daha küçük Y-değerlerine sahip noktalar okunması daha zor olacaktır.
# 20 tabanlı (1, 20, 400, 8000...) logaritmik ölçekleme
# çizilen noktaları yayacak ve değerlerini grafikte daha kolay okumamızı sağlayacaktır.
chart.axis_y.scaling.type = aw.drawing.charts.AxisScaleType.LOGARITHMIC
chart.axis_y.scaling.log_base = 20
doc.save(file_name=ARTIFACTS_DIR + 'Charts.AxisScaling.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [AxisScaling](../)

