---
title: ChartSeriesCollection.count property
linktitle: count property
articleTitle: count property
second_title: Aspose.Words for Python
description: "ChartSeriesCollection.count property. Returns the number of [ChartSeries](../../chartseries/) in this collection."
type: docs
weight: 20
url: /ar/python-net/aspose.words.drawing.charts/chartseriescollection/count/
---

## ChartSeriesCollection.count property

Returns the number of [ChartSeries](../../chartseries/) in this collection.



```python
@property
def count(self) -> int:
    ...

```

### Examples

Shows how to add and remove series data in a chart.

```python
# أدرج مخطط عمودي سيحتوي على ثلاث سلاسل من بيانات العرض التوضيحي بشكل افتراضي.
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
chart_shape = builder.insert_chart(chart_type=ChartType.COLUMN, width=400, height=300)
chart = chart_shape.chart
chart_data = chart.series
assert chart_data.count == 3
# اطبع اسم كل سلسلة في المخطط.
for series in chart.series:
    print(series.name)
# هذه هي أسماء الفئات في المخطط.
categories = ['Category 1', 'Category 2', 'Category 3', 'Category 4']
# يمكننا إضافة سلسلة بقيم جديدة للفئات الموجودة.
# سيحتوي هذا المخطط الآن على أربع مجموعات من أربعة أعمدة.
chart.series.add(series_name='Series 4', categories=categories, values=[4.4, 7, 3.5, 2.1])
assert chart_data.count == 4
assert chart_data[3].name == 'Series 4'
# يمكن أيضًا إزالة سلسلة مخطط بواسطة الفهرس، مثل هذا.
# سيؤدي هذا إلى إزالة إحدى السلاسل الثلاثة للعرض التوضيحي التي جاءت مع المخطط.
chart_data.remove_at(2)
assert not any([s.name == 'Series 3' for s in chart_data])
assert chart_data.count == 3
assert chart_data[2].name == 'Series 4'
# يمكننا أيضًا مسح جميع بيانات المخطط دفعة واحدة باستخدام هذه الطريقة.
# عند إنشاء مخطط جديد، هذه هي الطريقة لمسح جميع بيانات العرض التوضيحي
# قبل أن نتمكن من البدء في العمل على مخطط فارغ.
chart_data.clear()
assert chart_data.count == 0
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartSeriesCollection](../)

