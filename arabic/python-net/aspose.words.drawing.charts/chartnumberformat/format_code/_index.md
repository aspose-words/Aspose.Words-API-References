---
title: ChartNumberFormat.format_code property
linktitle: format_code property
articleTitle: format_code property
second_title: Aspose.Words for Python
description: "ChartNumberFormat.format_code property. Gets or sets the format code applied to a data label."
type: docs
weight: 10
url: /ar/python-net/aspose.words.drawing.charts/chartnumberformat/format_code/
---

## ChartNumberFormat.format_code property

Gets or sets the format code applied to a data label.


```python
@property
def format_code(self) -> str:
    ...

@format_code.setter
def format_code(self, value: str):
    ...

```

### Remarks

Number formatting is used to change the way a value appears in data label and can be used in some very creative ways.
The examples of number formats:
Number - "#,##0.00"

Currency - "\\"$\\"#,##0.00"

Time - "[$-x-systime]h:mm:ss AM/PM"

Date - "d/mm/yyyy"

Percentage - "0.00%"

Fraction - "# ?/?"

Scientific - "0.00E+00"

Text - "@"

Accounting - "_-\\"$\\"\* #,##0.00_-;-\\"$\\"\* #,##0.00_-;_-\\"$\\"\* \\"-\\"??_-;_-@_-"

Custom with color - "[Red]-#,##0.0"




### Examples

Shows how to enable and configure data labels for a chart series.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# أضف مخططًا خطيًا، ثم امسح سلسلة البيانات التجريبية الخاصة به للبدء بمخطط نظيف،
# ثم قم بتعيين عنوان.
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.LINE, width=500, height=300)
chart = shape.chart
chart.series.clear()
chart.title.text = 'Monthly sales report'
# أدخل سلسلة مخطط مخصصة مع الأشهر كفئات للمحور X،
# ومبالغ عشرية مقابلة للمحور Y.
series = chart.series.add(series_name='Revenue', categories=['January', 'February', 'March'], values=[25.611, 21.439, 33.75])
# فعّل تسميات البيانات، ثم طبّق تنسيق رقم مخصص للقيم المعروضة في تسميات البيانات.
# سيعامل هذا التنسيق القيم العشرية المعروضة كملايين من الدولارات الأمريكية.
series.has_data_labels = True
data_labels = series.data_labels
data_labels.show_value = True
data_labels.number_format.format_code = '"US$" #,##0.000"M"'
data_labels.font.size = 12
doc.save(file_name=ARTIFACTS_DIR + 'Charts.DataLabelNumberFormat.docx')
```

Shows how to set formatting for chart values.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.COLUMN, width=500, height=300)
chart = shape.chart
# مسح سلسلة بيانات العرض التجريبية للمخطط للبدء بمخطط نظيف.
chart.series.clear()
# أضف سلسلة مخصصة إلى المخطط مع فئات لمحور X،
# وقيم عددية كبيرة ذات صلة لمحور Y.
chart.series.add(series_name='Aspose Test Series', categories=['Word', 'PDF', 'Excel', 'GoogleDocs', 'Note'], values=[1900000, 850000, 2100000, 600000, 1500000])
# اضبط تنسيق الأرقام لتسميات علامات محور Y بحيث لا يتم تجميع الأرقام بفواصل.
chart.axis_y.number_format.format_code = '#,##0'
# يمكن لهذا العلم تجاوز القيمة السابقة واستخراج تنسيق الرقم من الخلية المصدر.
self.assertFalse(chart.axis_y.number_format.is_linked_to_source)
doc.save(file_name=ARTIFACTS_DIR + 'Charts.SetNumberFormatToChartAxis.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartNumberFormat](../)

