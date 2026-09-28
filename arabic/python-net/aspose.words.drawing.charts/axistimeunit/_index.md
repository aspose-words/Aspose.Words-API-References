---
title: AxisTimeUnit enumeration
linktitle: AxisTimeUnit enumeration
articleTitle: AxisTimeUnit enumeration
second_title: Aspose.Words for Python
description: "aspose.words.drawing.charts.AxisTimeUnit enumeration. Specifies the unit of time for axes."
type: docs
weight: 120
url: /ar/python-net/aspose.words.drawing.charts/axistimeunit/
---

## AxisTimeUnit enumeration

Specifies the unit of time for axes.


### Members

| Name | Description |
| --- | --- |
| AUTOMATIC | Specifies that unit was not set explicitly and default value should be used. |
| DAYS | Specifies that the chart data shall be shown in days. |
| MONTHS | Specifies that the chart data shall be shown in months. |
| YEARS | Specifies that the chart data shall be shown in years. |

### Examples

Shows how to insert chart with date/time values.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.LINE, width=500, height=300)
chart = shape.chart
# مسح سلسلة بيانات العرض التجريبية للمخطط للبدء بمخطط نظيف.
chart.series.clear()
# أضف سلسلة مخصصة تحتوي على قيم تاريخ/وقت لمحور X، وقيم عشرية ذات صلة لمحور Y.
chart.series.add_date(series_name='Aspose Test Series', dates=[datetime.datetime(2017, 11, 6), datetime.datetime(2017, 11, 9), datetime.datetime(2017, 11, 15), datetime.datetime(2017, 11, 21), datetime.datetime(2017, 11, 25), datetime.datetime(2017, 11, 29)], values=[1.2, 0.3, 2.1, 2.9, 4.2, 5.3])
# حدد الحدود السفلية والعلوية لمحور X.
x_axis = chart.axis_x
# حوّل تاريخ/وقت إلى تاريخ OLE Automation (أيام منذ 1899-12-30)

def to_ole_autodate(dt):
    # عدد الأيام من 0001-01-01 إلى 1899-12-30 هو 693594
    delta = dt - datetime.datetime(1899, 12, 30)
    return delta.days + (dt.hour * 3600 + dt.minute * 60 + dt.second) / 86400.0
x_axis.scaling.minimum = aw.drawing.charts.AxisBound(to_ole_autodate(datetime.datetime(2017, 11, 5)))
x_axis.scaling.maximum = aw.drawing.charts.AxisBound(to_ole_autodate(datetime.datetime(2017, 12, 3)))
# اضبط الوحدات الرئيسية لمحور X إلى أسبوع، والوحدات الفرعية إلى يوم.
x_axis.base_time_unit = aw.drawing.charts.AxisTimeUnit.DAYS
x_axis.major_unit = 7
x_axis.major_tick_mark = aw.drawing.charts.AxisTickMark.CROSS
x_axis.minor_unit = 1
x_axis.minor_tick_mark = aw.drawing.charts.AxisTickMark.OUTSIDE
x_axis.has_major_gridlines = True
x_axis.has_minor_gridlines = True
# عرّف خصائص محور Y للقيم العشرية.
y_axis = chart.axis_y
y_axis.tick_labels.position = aw.drawing.charts.AxisTickLabelPosition.HIGH
y_axis.major_unit = 100
y_axis.minor_unit = 50
y_axis.display_unit.unit = aw.drawing.charts.AxisBuiltInUnit.HUNDREDS
y_axis.scaling.minimum = aw.drawing.charts.AxisBound(100)
y_axis.scaling.maximum = aw.drawing.charts.AxisBound(700)
y_axis.has_major_gridlines = True
y_axis.has_minor_gridlines = True
doc.save(file_name=ARTIFACTS_DIR + 'Charts.DateTimeValues.docx')
```

### See Also

* module [aspose.words.drawing.charts](../)

