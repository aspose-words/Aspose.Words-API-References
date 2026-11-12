---
title: ChartDataLabelCollection.number_format property
linktitle: number_format property
articleTitle: number_format property
second_title: Aspose.Words for Python
description: "ChartDataLabelCollection.number_format property. Gets an [ChartNumberFormat](../../chartnumberformat/) instance allowing to set number format for the data labels of the entire series."
type: docs
weight: 50
url: /ru/python-net/aspose.words.drawing.charts/chartdatalabelcollection/number_format/
---

## ChartDataLabelCollection.number_format property

Gets an [ChartNumberFormat](../../chartnumberformat/) instance allowing to set number format for the data labels of the
entire series.



```python
@property
def number_format(self) -> aspose.words.drawing.charts.ChartNumberFormat:
    ...

```

### Examples

Shows how to enable and configure data labels for a chart series.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Добавьте линейную диаграмму, затем очистите её демонстрационную серию данных, чтобы начать с чистой диаграммы,
# а затем задайте заголовок.
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.LINE, width=500, height=300)
chart = shape.chart
chart.series.clear()
chart.title.text = 'Monthly sales report'
# Вставьте пользовательскую серию диаграммы с месяцами в качестве категорий для оси X,
# и соответствующими десятичными значениями для оси Y.
series = chart.series.add(series_name='Revenue', categories=['January', 'February', 'March'], values=[25.611, 21.439, 33.75])
# Включите подписи данных, а затем примените пользовательский числовой формат для значений, отображаемых в подписях данных.
# Этот формат будет воспринимать отображаемые десятичные значения как миллионы долларов США.
series.has_data_labels = True
data_labels = series.data_labels
data_labels.show_value = True
data_labels.number_format.format_code = '"US$" #,##0.000"M"'
data_labels.font.size = 12
doc.save(file_name=ARTIFACTS_DIR + 'Charts.DataLabelNumberFormat.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartDataLabelCollection](../)

