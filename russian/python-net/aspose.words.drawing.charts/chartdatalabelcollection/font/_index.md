---
title: ChartDataLabelCollection.font property
linktitle: font property
articleTitle: font property
second_title: Aspose.Words for Python
description: "ChartDataLabelCollection.font property. Provides access to the font formatting of the data labels of the entire series."
type: docs
weight: 30
url: /ru/python-net/aspose.words.drawing.charts/chartdatalabelcollection/font/
---

## ChartDataLabelCollection.font property

Provides access to the font formatting of the data labels of the entire series.


```python
@property
def font(self) -> aspose.words.Font:
    ...

```

### Remarks

Value defined for this property can be overridden for an individual data label with using the
[ChartDataLabel.font](../../chartdatalabel/font/) property.



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

