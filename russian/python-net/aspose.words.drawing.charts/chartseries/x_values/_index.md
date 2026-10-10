---
title: ChartSeries.x_values property
linktitle: x_values property
articleTitle: x_values property
second_title: Aspose.Words for Python
description: "ChartSeries.x_values property. Gets a collection of X values for this chart series."
type: docs
weight: 140
url: /ru/python-net/aspose.words.drawing.charts/chartseries/x_values/
---

## ChartSeries.x_values property

Gets a collection of X values for this chart series.


```python
@property
def x_values(self) -> aspose.words.drawing.charts.ChartXValueCollection:
    ...

```

### Examples

Shows how to work with the format code of the chart data.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Вставьте пузырьковую диаграмму.
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.BUBBLE, width=432, height=252)
chart = shape.chart
# Удалить автоматически сгенерированную серию.
chart.series.clear()
series = chart.series.add_bubbles(series_name='Series1', x_values=[1, 1.9, 2.45, 3], y_values=[1, -0.9, 1.82, 0], bubble_sizes=[2, 1.1, 2.95, 2])
# Показать подписи данных.
series.has_data_labels = True
series.data_labels.show_category_name = True
series.data_labels.show_value = True
series.data_labels.show_bubble_size = True
# Установите коды формата данных.
series.x_values.format_code = '#,##0.0#'
series.y_values.format_code = '#,##0.0#;[Red]\\-#,##0.0#'
series.bubble_sizes.format_code = '#,##0.0#'
doc.save(file_name=ARTIFACTS_DIR + 'Charts.FormatCode.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartSeries](../)

