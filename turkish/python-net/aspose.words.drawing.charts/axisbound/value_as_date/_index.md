---
title: AxisBound.value_as_date property
linktitle: value_as_date property
articleTitle: value_as_date property
second_title: Aspose.Words for Python
description: "AxisBound.value_as_date property. Returns value of axis bound represented as datetime."
type: docs
weight: 40
url: /tr/python-net/aspose.words.drawing.charts/axisbound/value_as_date/
---

## AxisBound.value_as_date property

Returns value of axis bound represented as datetime.


```python
@property
def value_as_date(self) -> datetime.datetime:
    ...

```

### Examples

Shows how to set custom axis bounds.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
chart_shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.SCATTER, width=450, height=300)
chart = chart_shape.chart
# Temiz bir grafikle başlamak için grafiğin demo veri serilerini temizleyin.
chart.series.clear()
# İki ondalık dizi içeren bir seri ekleyin. İlk dizi X değerlerini içerir,
# ve ikincisi, dağılım grafiğindeki noktalar için karşılık gelen Y değerlerini içerir.
chart.series.add_double(series_name='Series 1', x_values=[1.1, 5.4, 7.9, 3.5, 2.1, 9.7], y_values=[2.1, 0.3, 0.6, 3.3, 1.4, 1.9])
# Varsayılan olarak, grafiğin X ve Y eksenlerine varsayılan ölçekleme uygulanır,
# böylece her iki eksenin aralıkları, her serinin tüm X ve Y değerlerini kapsayacak kadar geniş olur.
self.assertTrue(chart.axis_x.scaling.minimum.is_auto)
# Kendi eksen sınırlarımızı tanımlayabiliriz.
# Bu durumda, X ve Y ekseni cetvellerinin her ikisinin de 0 ile 10 arasında bir aralık göstermesini sağlayacağız.
chart.axis_x.scaling.minimum = aw.drawing.charts.AxisBound(value=0)
chart.axis_x.scaling.maximum = aw.drawing.charts.AxisBound(value=10)
chart.axis_y.scaling.minimum = aw.drawing.charts.AxisBound(value=0)
chart.axis_y.scaling.maximum = aw.drawing.charts.AxisBound(value=10)
self.assertFalse(chart.axis_x.scaling.minimum.is_auto)
self.assertFalse(chart.axis_y.scaling.minimum.is_auto)
# X ekseninde tarih aralığı ve Y ekseninde ondalık değerler gerektiren bir seriyle bir çizgi grafik oluşturun.
chart_shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.LINE, width=450, height=300)
chart = chart_shape.chart
chart.series.clear()
dates = [datetime.datetime(1973, 5, 11), datetime.datetime(1981, 2, 4), datetime.datetime(1985, 9, 23), datetime.datetime(1989, 6, 28), datetime.datetime(1994, 12, 15)]
chart.series.add_date(series_name='Series 1', dates=dates, values=[3, 4.7, 5.9, 7.1, 8.9])
# Ayrıca eksen sınırlarını tarih biçiminde ayarlayarak grafiği belirli bir döneme sınırlayabiliriz.
# Aralığı 1980-1990 olarak ayarlamak, serinin iki değerini dışarı bırakacaktır
# bu değerler grafiğin aralığının dışındadır.
chart.axis_x.scaling.minimum = aw.drawing.charts.AxisBound(datetime=datetime.datetime(1980, 1, 1))
chart.axis_x.scaling.maximum = aw.drawing.charts.AxisBound(datetime=datetime.datetime(1990, 1, 1))
doc.save(file_name=ARTIFACTS_DIR + 'Charts.AxisBound.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [AxisBound](../)

