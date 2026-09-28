---
title: ChartDataPointCollection.has_default_format method
linktitle: has_default_format method
articleTitle: has_default_format method
second_title: Aspose.Words for Python
description: "ChartDataPointCollection.has_default_format method. Gets a flag indicating whether the data point at the specified index has default format."
type: docs
weight: 50
url: /ar/python-net/aspose.words.drawing.charts/chartdatapointcollection/has_default_format/
---

## has_default_format(data_point_index) {#int}

Gets a flag indicating whether the data point at the specified index has default format.


```python
def has_default_format(self, data_point_index: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| data_point_index | int |  |

### Examples

Shows how to copy data point format.

```python
doc = aw.Document(file_name=MY_DIR + 'DataPoint format.docx')
# جعل المخطط والسلسلة يحدثان التنسيق.
shape = doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape()
series = shape.chart.series[0]
data_points = series.data_points
self.assertTrue(data_points.has_default_format(0))
self.assertFalse(data_points.has_default_format(1))
# نسخ تنسيق نقطة البيانات ذات الفهرس 1 إلى نقطة البيانات ذات الفهرس 2
# بحيث يبدو نقطة البيانات 2 نفسها مثل نقطة البيانات 1.
data_points.copy_format(0, 1)
self.assertTrue(data_points.has_default_format(0))
self.assertTrue(data_points.has_default_format(1))
# انسخ تنسيق نقطة البيانات ذات الفهرس 0 إلى الإعدادات الافتراضية للسلسلة بحيث تكون جميع نقاط البيانات
# في السلسلة التي لديها التنسيق الافتراضي تبدو نفسها مثل نقطة البيانات 0.
series.copy_format_from(1)
self.assertTrue(data_points.has_default_format(0))
self.assertTrue(data_points.has_default_format(1))
doc.save(file_name=ARTIFACTS_DIR + 'Charts.CopyDataPointFormat.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartDataPointCollection](../)

