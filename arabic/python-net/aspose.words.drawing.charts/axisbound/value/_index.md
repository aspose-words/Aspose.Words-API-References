---
title: AxisBound.value property
linktitle: value property
articleTitle: value property
second_title: Aspose.Words for Python
description: "AxisBound.value property. Returns numeric value of axis bound."
type: docs
weight: 30
url: /ar/python-net/aspose.words.drawing.charts/axisbound/value/
---

## AxisBound.value property

Returns numeric value of axis bound.


```python
@property
def value(self) -> float:
    ...

```

### Examples

Shows how to set custom axis bounds.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
chart_shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.SCATTER, width=450, height=300)
chart = chart_shape.chart
# مسح سلسلة بيانات العرض التجريبية للمخطط للبدء بمخطط نظيف.
chart.series.clear()
# أضف سلسلة تحتوي على مصفوفتين عشريتين. المصفوفة الأولى تحتوي على قيم X،
# والثانية تحتوي على قيم Y المقابلة للنقاط في مخطط التبعثر.
chart.series.add_double(series_name='Series 1', x_values=[1.1, 5.4, 7.9, 3.5, 2.1, 9.7], y_values=[2.1, 0.3, 0.6, 3.3, 1.4, 1.9])
# بشكل افتراضي، يتم تطبيق التحجيم الافتراضي على محوري X و Y للرسم البياني،
# بحيث تكون نطاقاتهما كبيرة بما يكفي لتشمل كل قيمة X و Y لكل سلسلة.
self.assertTrue(chart.axis_x.scaling.minimum.is_auto)
# يمكننا تعريف حدود المحاور الخاصة بنا.
# في هذه الحالة، سنجعل كل من محوري X و Y يعرضان نطاقًا من 0 إلى 10.
chart.axis_x.scaling.minimum = aw.drawing.charts.AxisBound(value=0)
chart.axis_x.scaling.maximum = aw.drawing.charts.AxisBound(value=10)
chart.axis_y.scaling.minimum = aw.drawing.charts.AxisBound(value=0)
chart.axis_y.scaling.maximum = aw.drawing.charts.AxisBound(value=10)
self.assertFalse(chart.axis_x.scaling.minimum.is_auto)
self.assertFalse(chart.axis_y.scaling.minimum.is_auto)
# أنشئ مخططًا خطيًا بسلسلة تحتاج إلى نطاق من التواريخ على محور X، وقيم عشرية على محور Y.
chart_shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.LINE, width=450, height=300)
chart = chart_shape.chart
chart.series.clear()
dates = [datetime.datetime(1973, 5, 11), datetime.datetime(1981, 2, 4), datetime.datetime(1985, 9, 23), datetime.datetime(1989, 6, 28), datetime.datetime(1994, 12, 15)]
chart.series.add_date(series_name='Series 1', dates=dates, values=[3, 4.7, 5.9, 7.1, 8.9])
# يمكننا أيضًا ضبط حدود المحاور على شكل تواريخ، لتحديد المخطط بفترة زمنية.
# ضبط النطاق إلى 1980-1990 سيحذف قيمتين من قيم السلسلة
# التي تقع خارج النطاق في الرسم البياني.
chart.axis_x.scaling.minimum = aw.drawing.charts.AxisBound(datetime=datetime.datetime(1980, 1, 1))
chart.axis_x.scaling.maximum = aw.drawing.charts.AxisBound(datetime=datetime.datetime(1990, 1, 1))
doc.save(file_name=ARTIFACTS_DIR + 'Charts.AxisBound.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [AxisBound](../)

