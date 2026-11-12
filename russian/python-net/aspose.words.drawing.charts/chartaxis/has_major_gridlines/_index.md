---
title: ChartAxis.has_major_gridlines property
linktitle: has_major_gridlines property
articleTitle: has_major_gridlines property
second_title: Aspose.Words for Python
description: "ChartAxis.has_major_gridlines property. Gets or sets a flag indicating whether the axis has major gridlines."
type: docs
weight: 90
url: /ru/python-net/aspose.words.drawing.charts/chartaxis/has_major_gridlines/
---

## ChartAxis.has_major_gridlines property

Gets or sets a flag indicating whether the axis has major gridlines.


```python
@property
def has_major_gridlines(self) -> bool:
    ...

@has_major_gridlines.setter
def has_major_gridlines(self, value: bool):
    ...

```

### Examples

Shows how to insert chart with date/time values.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.LINE, width=500, height=300)
chart = shape.chart
# Очистите демонстрационные данные серии диаграммы, чтобы начать с чистой диаграммы.
chart.series.clear()
# Добавьте пользовательскую серию, содержащую значения даты/времени для оси X, и соответствующие десятичные значения для оси Y.
chart.series.add_date(series_name='Aspose Test Series', dates=[datetime.datetime(2017, 11, 6), datetime.datetime(2017, 11, 9), datetime.datetime(2017, 11, 15), datetime.datetime(2017, 11, 21), datetime.datetime(2017, 11, 25), datetime.datetime(2017, 11, 29)], values=[1.2, 0.3, 2.1, 2.9, 4.2, 5.3])
# Установите нижние и верхние границы для оси X.
x_axis = chart.axis_x
# Преобразуйте дату и время в дату OLE Automation (дни с 30‑12‑1899)

def to_ole_autodate(dt):
    # Количество дней с 01‑01‑0001 по 30‑12‑1899 равно 693594
    delta = dt - datetime.datetime(1899, 12, 30)
    return delta.days + (dt.hour * 3600 + dt.minute * 60 + dt.second) / 86400.0
x_axis.scaling.minimum = aw.drawing.charts.AxisBound(to_ole_autodate(datetime.datetime(2017, 11, 5)))
x_axis.scaling.maximum = aw.drawing.charts.AxisBound(to_ole_autodate(datetime.datetime(2017, 12, 3)))
# Установите основные единицы оси X как неделю, а вспомогательные единицы — как день.
x_axis.base_time_unit = aw.drawing.charts.AxisTimeUnit.DAYS
x_axis.major_unit = 7
x_axis.major_tick_mark = aw.drawing.charts.AxisTickMark.CROSS
x_axis.minor_unit = 1
x_axis.minor_tick_mark = aw.drawing.charts.AxisTickMark.OUTSIDE
x_axis.has_major_gridlines = True
x_axis.has_minor_gridlines = True
# Определите свойства оси Y для десятичных значений.
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

* module [aspose.words.drawing.charts](../../)
* class [ChartAxis](../)

