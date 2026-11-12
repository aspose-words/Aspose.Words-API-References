---
title: ChartDataPoint.clear_format method
linktitle: clear_format method
articleTitle: clear_format method
second_title: Aspose.Words for Python
description: "ChartDataPoint.clear_format method. Clears format of this data point"
type: docs
weight: 70
url: /tr/python-net/aspose.words.drawing.charts/chartdatapoint/clear_format/
---

## clear_format() {#default}

Clears format of this data point. The properties are set to the default values defined in the parent series.


```python
def clear_format(self):
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
# Grafiğin veri noktalarını elmas şekli gibi göstererek vurgula.
for series in chart.series:
    ExCharts._apply_data_points(series, 4, aw.drawing.charts.MarkerSymbol.DIAMOND, 15)
# İlk veri serisini temsil eden çizgiyi yumuşat.
chart.series[0].smooth = True
# İlk serinin veri noktalarının değeri negatif olduğunda renklerinin tersine dönmeyeceğini doğrula.
for data_point in chart.series[0].data_points:
    assert not data_point.invert_if_negative
data_point = chart.series[1].data_points[2]
data_point.format.fill.color = drawing.Color.red
# Daha temiz bir grafik görünümü için biçimi tek tek temizleyebiliriz.
data_point.clear_format()
# Ayrıca bir bütün veri serisinin tüm veri noktalarını bir kerede kaldırabiliriz.
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

