---
title: ChartDataPoint.format property
linktitle: format property
articleTitle: format property
second_title: Aspose.Words for Python
description: "ChartDataPoint.format property. Provides access to fill and line formatting of this data point."
type: docs
weight: 30
url: /sv/python-net/aspose.words.drawing.charts/chartdatapoint/format/
---

## ChartDataPoint.format property

Provides access to fill and line formatting of this data point.


```python
@property
def format(self) -> aspose.words.drawing.charts.ChartFormat:
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

Shows how to set individual formatting for categories of a column chart.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.COLUMN, width=432, height=252)
chart = shape.chart
# Ta bort standardgenererad serie.
chart.series.clear()
# Lägger till ny serie.
series = chart.series.add(series_name='Series 1', categories=['Category 1', 'Category 2', 'Category 3', 'Category 4'], values=[1, 2, 3, 4])
# Ställ in kolumnformatering.
data_points = series.data_points
data_points[0].format.fill.preset_textured(aw.drawing.PresetTexture.DENIM)
data_points[1].format.fill.fore_color = aspose.pydrawing.Color.red
data_points[2].format.fill.fore_color = aspose.pydrawing.Color.yellow
data_points[3].format.fill.fore_color = aspose.pydrawing.Color.blue
doc.save(file_name=ARTIFACTS_DIR + 'Charts.DataPointsFormatting.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartDataPoint](../)

