---
title: AxisScaling.type property
linktitle: type property
articleTitle: type property
second_title: Aspose.Words for Python
description: "AxisScaling.type property. Gets or sets scaling type of the axis."
type: docs
weight: 50
url: /tr/python-net/aspose.words.drawing.charts/axisscaling/type/
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

