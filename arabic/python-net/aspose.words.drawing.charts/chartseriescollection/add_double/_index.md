---
title: ChartSeriesCollection.add_double method
linktitle: add_double method
articleTitle: add_double method
second_title: Aspose.Words for Python
description: "aspose.words.drawing.charts.ChartSeriesCollection.add_double method"
type: docs
weight: 60
url: /ar/python-net/aspose.words.drawing.charts/chartseriescollection/add_double/
---

## add_double(series_name, x_values, y_values) {#str_floatlist_floatlist}

Adds new [ChartSeries](../../chartseries/) to this collection.
Use this method to add series to any type of Scatter charts.



```python
def add_double(self, series_name: str, x_values: List[float], y_values: List[float]):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| series_name | str |  |
| x_values | List[float] |  |
| y_values | List[float] |  |

### Returns

Recently added [ChartSeries](../../chartseries/) object.


## add_double(series_name, x_values) {#str_floatlist}

Adds new [ChartSeries](../../chartseries/) to this collection.
Use this method to add series to Histogram charts.



```python
def add_double(self, series_name: str, x_values: List[float]):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| series_name | str |  |
| x_values | List[float] |  |

### Remarks

For chart types other than Histogram, this method adds a series with empty Y values.


### Returns

Recently added [ChartSeries](../../chartseries/) object.


## Examples

Shows how to create an appropriate type of chart series for a graph type.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# هناك عدة طرق لملء مجموعة سلاسل المخطط.
# يُقصد من مخططات السلاسل المختلفة أن تُستخدم لأنواع المخططات المختلفة.
# 1 - مخطط عمودي مع أعمدة مُجمعة ومُقسمة على محور X حسب الفئة:
chart = ExCharts._append_chart(builder, aw.drawing.charts.ChartType.COLUMN, 500, 300)
categories = ['Category 1', 'Category 2', 'Category 3']
# أدرج سلسلتين من القيم العشرية تحتوي كل منهما على قيمة لكل فئة على حدة.
# سيحتوي هذا المخطط العمودي على ثلاث مجموعات، كل مجموعة بها عمودان.
chart.series.add(series_name='Series 1', categories=categories, values=[76.6, 82.1, 91.6])
chart.series.add(series_name='Series 2', categories=categories, values=[64.2, 79.5, 94])
# تُوزَّع الفئات على محور X، وتُوزَّع القيم على محور Y.
self.assertEqual(aw.drawing.charts.ChartAxisType.CATEGORY, chart.axis_x.type)
self.assertEqual(aw.drawing.charts.ChartAxisType.VALUE, chart.axis_y.type)
# 2 - مخطط مساحي مع توزع التواريخ على محور X:
chart = ExCharts._append_chart(builder, aw.drawing.charts.ChartType.AREA, 500, 300)
dates = [datetime.datetime(2014, 3, 31), datetime.datetime(2017, 1, 23), datetime.datetime(2017, 6, 18), datetime.datetime(2019, 11, 22), datetime.datetime(2020, 9, 7)]
# أدرج سلسلة بقيمة عشرية لكل تاريخ على حدة.
# ستُوزَّع التواريخ على محور X خطي،
# والقيم المضافة إلى هذه السلسلة ستُنشئ نقاط بيانات.
chart.series.add_date(series_name='Series 1', dates=dates, values=[15.8, 21.5, 22.9, 28.7, 33.1])
self.assertEqual(aw.drawing.charts.ChartAxisType.CATEGORY, chart.axis_x.type)
self.assertEqual(aw.drawing.charts.ChartAxisType.VALUE, chart.axis_y.type)
# 3 - مخطط مبعثر ثنائي الأبعاد:
chart = ExCharts._append_chart(builder, aw.drawing.charts.ChartType.SCATTER, 500, 300)
# كل سلسلة ستحتاج إلى مصفوفتين عشريتين متساويتين في الطول.
# المصفوفة الأولى تحتوي على قيم X، والمصفوفة الثانية تحتوي على قيم Y المقابلة.
# لنقاط البيانات على رسم المخطط.
chart.series.add_double(series_name='Series 1', x_values=[3.1, 3.5, 6.3, 4.1, 2.2, 8.3, 1.2, 3.6], y_values=[3.1, 6.3, 4.6, 0.9, 8.5, 4.2, 2.3, 9.9])
chart.series.add_double(series_name='Series 2', x_values=[2.6, 7.3, 4.5, 6.6, 2.1, 9.3, 0.7, 3.3], y_values=[7.1, 6.6, 3.5, 7.8, 7.7, 9.5, 1.3, 4.6])
self.assertEqual(aw.drawing.charts.ChartAxisType.VALUE, chart.axis_x.type)
self.assertEqual(aw.drawing.charts.ChartAxisType.VALUE, chart.axis_y.type)
# 4 - مخطط الفقاعات:
chart = ExCharts._append_chart(builder, aw.drawing.charts.ChartType.BUBBLE, 500, 300)
# كل سلسلة ستحتاج إلى ثلاث مصفوفات عشرية متساوية في الطول.
# المصفوفة الأولى تحتوي على قيم X، والثانية تحتوي على قيم Y المقابلة،
# والثالثة تحتوي على الأقطار لكل نقطة بيانات في الرسم.
chart.series.add_bubbles(series_name='Series 1', x_values=[1.1, 5, 9.8], y_values=[1.2, 4.9, 9.9], bubble_sizes=[2, 4, 8])
doc.save(file_name=ARTIFACTS_DIR + 'Charts.ChartSeriesCollection.docx')
```

Shows how to create an appropriate type of chart series for a graph type (AppendChart).

```python
@staticmethod
def _append_chart(builder, chart_type, width, height):
    chart_shape = builder.insert_chart(chart_type=chart_type, width=width, height=height)
    chart = chart_shape.chart
    chart.series.clear()
    return chart
```

Shows how to create histogram chart.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# أدرج مخطط المدرج التكراري.
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.HISTOGRAM, width=450, height=450)
chart = shape.chart
chart.title.text = 'Avg Temperature since 1991'
# احذف السلسلة التي تم إنشاؤها افتراضيًا.
chart.series.clear()
# إضافة سلسلة.
chart.series.add_double(series_name='Avg Temperature', x_values=[51.8, 53.6, 50.3, 54.7, 53.9, 54.3, 53.4, 52.9, 53.3, 53.7, 53.8, 52, 55, 52.1, 53.4, 53.8, 53.8, 51.9, 52.1, 52.7, 51.8, 56.6, 53.3, 55.6, 56.3, 56.2, 56.1, 56.2, 53.6, 55.7, 56.3, 55.9, 55.6])
doc.save(file_name=ARTIFACTS_DIR + 'Charts.Histogram.docx')
```

## See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartSeriesCollection](../)

