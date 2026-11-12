---
title: ChartMarker.size property
linktitle: size property
articleTitle: size property
second_title: Aspose.Words for Python
description: "ChartMarker.size property. Gets or sets chart marker size"
type: docs
weight: 20
url: /ru/python-net/aspose.words.drawing.charts/chartmarker/size/
---

## ChartMarker.size property

Gets or sets chart marker size.
Default value is 7.


```python
@property
def size(self) -> int:
    ...

@size.setter
def size(self, value: int):
    ...

```

### Examples

Shows how to work with data points on a line chart.

```python
from api_example_base import ApiExampleBase, ARTIFACTS_DIR
import aspose.words as aw
import aspose.pydrawing as drawing
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.LINE, width=500, height=350)
chart = shape.chart
self.assertEqual(3, chart.series.count)
self.assertEqual('Series 1', chart.series[0].name)
self.assertEqual('Series 2', chart.series[1].name)
self.assertEqual('Series 3', chart.series[2].name)
# Выделить точки данных диаграммы, сделав их в виде ромбов.
for series in chart.series:
    ExCharts._apply_data_points(series, 4, aw.drawing.charts.MarkerSymbol.DIAMOND, 15)
# Сгладить линию, представляющую первую серию данных.
chart.series[0].smooth = True
# Проверьте, что точки данных первой серии не изменят цвета, если значение отрицательное.
for data_point in chart.series[0].data_points:
    assert not data_point.invert_if_negative
data_point = chart.series[1].data_points[2]
data_point.format.fill.color = drawing.Color.red
# Для более чистого вида графика мы можем очищать формат по отдельности.
data_point.clear_format()
# Мы также можем полностью удалить всю серию точек данных за один раз.
chart.series[2].data_points.clear_format()
doc.save(file_name=ARTIFACTS_DIR + 'Charts.ChartDataPoint.docx')
```

Shows how to work with data points on a line chart (ApplyDataPoints).

```python
@staticmethod
def _apply_data_points(series, data_points_count, marker_symbol, data_point_size):
    i = 0
    while i < data_points_count:
        point = series.data_points[i]
        point.marker.symbol = marker_symbol
        point.marker.size = data_point_size
        assert i == point.index
        i += 1
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartMarker](../)

