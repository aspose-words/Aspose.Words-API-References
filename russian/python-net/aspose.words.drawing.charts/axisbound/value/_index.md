---
title: AxisBound.value property
linktitle: value property
articleTitle: value property
second_title: Aspose.Words for Python
description: "AxisBound.value property. Returns numeric value of axis bound."
type: docs
weight: 30
url: /ru/python-net/aspose.words.drawing.charts/axisbound/value/
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
# Очистите демонстрационные данные серии диаграммы, чтобы начать с чистой диаграммы.
chart.series.clear()
# Добавьте серию с двумя массивами десятичных чисел. Первый массив содержит значения X,
# а второй содержит соответствующие значения Y для точек в диаграмме рассеяния.
chart.series.add_double(series_name='Series 1', x_values=[1.1, 5.4, 7.9, 3.5, 2.1, 9.7], y_values=[2.1, 0.3, 0.6, 3.3, 1.4, 1.9])
# По умолчанию к осям X и Y графика применяется масштабирование по умолчанию,
# чтобы их диапазоны были достаточно большими, чтобы охватить каждое значение X и Y каждой серии.
self.assertTrue(chart.axis_x.scaling.minimum.is_auto)
# Мы можем задать собственные границы осей.
# В этом случае мы установим диапазон от 0 до 10 для обеих осей X и Y.
chart.axis_x.scaling.minimum = aw.drawing.charts.AxisBound(value=0)
chart.axis_x.scaling.maximum = aw.drawing.charts.AxisBound(value=10)
chart.axis_y.scaling.minimum = aw.drawing.charts.AxisBound(value=0)
chart.axis_y.scaling.maximum = aw.drawing.charts.AxisBound(value=10)
self.assertFalse(chart.axis_x.scaling.minimum.is_auto)
self.assertFalse(chart.axis_y.scaling.minimum.is_auto)
# Создайте линейную диаграмму с серией, требующей диапазона дат по оси X и десятичных значений по оси Y.
chart_shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.LINE, width=450, height=300)
chart = chart_shape.chart
chart.series.clear()
dates = [datetime.datetime(1973, 5, 11), datetime.datetime(1981, 2, 4), datetime.datetime(1985, 9, 23), datetime.datetime(1989, 6, 28), datetime.datetime(1994, 12, 15)]
chart.series.add_date(series_name='Series 1', dates=dates, values=[3, 4.7, 5.9, 7.1, 8.9])
# Мы также можем задать границы осей в виде дат, ограничивая диаграмму определённым периодом.
# Установка диапазона 1980‑1990 исключит два значения серии
# которые находятся за пределами диапазона графика.
chart.axis_x.scaling.minimum = aw.drawing.charts.AxisBound(datetime=datetime.datetime(1980, 1, 1))
chart.axis_x.scaling.maximum = aw.drawing.charts.AxisBound(datetime=datetime.datetime(1990, 1, 1))
doc.save(file_name=ARTIFACTS_DIR + 'Charts.AxisBound.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [AxisBound](../)

