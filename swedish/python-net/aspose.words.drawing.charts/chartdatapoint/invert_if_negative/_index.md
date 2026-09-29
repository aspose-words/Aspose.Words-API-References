---
title: ChartDataPoint.invert_if_negative property
linktitle: invert_if_negative property
articleTitle: invert_if_negative property
second_title: Aspose.Words for Python
description: "ChartDataPoint.invert_if_negative property. Specifies whether the parent element shall inverts its colors if the value is negative."
type: docs
weight: 50
url: /sv/python-net/aspose.words.drawing.charts/chartdatapoint/invert_if_negative/
---

## ChartDataPoint.invert_if_negative property

Specifies whether the parent element shall inverts its colors if the value is negative.


```python
@property
def invert_if_negative(self) -> bool:
    ...

@invert_if_negative.setter
def invert_if_negative(self, value: bool):
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
# Betona diagrammets datapunkter genom att låta dem visas som diamantformer.
for series in chart.series:
    ExCharts._apply_data_points(series, 4, aw.drawing.charts.MarkerSymbol.DIAMOND, 15)
# Jämna ut linjen som representerar den första dataserien.
chart.series[0].smooth = True
# Verifiera att datapunkterna för den första serien inte inverterar sina färger om värdet är negativt.
for data_point in chart.series[0].data_points:
    assert not data_point.invert_if_negative
data_point = chart.series[1].data_points[2]
data_point.format.fill.color = drawing.Color.red
# För ett renare diagram kan vi rensa formatet individuellt.
data_point.clear_format()
# Vi kan också ta bort en hel serie av datapunkter på en gång.
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
* class [ChartDataPoint](../)

