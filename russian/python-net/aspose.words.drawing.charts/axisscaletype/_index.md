---
title: AxisScaleType enumeration
linktitle: AxisScaleType enumeration
articleTitle: AxisScaleType enumeration
second_title: Aspose.Words for Python
description: "aspose.words.drawing.charts.AxisScaleType enumeration. Specifies the possible scale types for an axis."
type: docs
weight: 70
url: /ru/python-net/aspose.words.drawing.charts/axisscaletype/
---

## AxisScaleType enumeration

Specifies the possible scale types for an axis.


### Members

| Name | Description |
| --- | --- |
| LINEAR | Linear scaling. |
| LOGARITHMIC | Logarithmic scaling. |

### Examples

Shows how to apply logarithmic scaling to a chart axis.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
chart_shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.SCATTER, width=450, height=300)
chart = chart_shape.chart
# Очистите демонстрационные данные серии диаграммы, чтобы начать с чистой диаграммы.
chart.series.clear()
# Вставьте серию с координатами X/Y для пяти точек.
chart.series.add_double(series_name='Series 1', x_values=[1, 2, 3, 4, 5], y_values=[1, 20, 400, 8000, 160000])
# Масштабирование оси X по умолчанию линейное,
# отображая равномерно увеличивающиеся значения, покрывающие диапазон наших X-значений (0, 1, 2, 3...).
# Линейная ось не идеальна для наших значений Y
# поскольку точки с меньшими значениями Y будет труднее читать.
# Логарифмическое масштабирование с основанием 20 (1, 20, 400, 8000...)
# распространит построенные точки, позволяя нам легче считывать их значения на диаграмме.
chart.axis_y.scaling.type = aw.drawing.charts.AxisScaleType.LOGARITHMIC
chart.axis_y.scaling.log_base = 20
doc.save(file_name=ARTIFACTS_DIR + 'Charts.AxisScaling.docx')
```

### See Also

* module [aspose.words.drawing.charts](../)

