---
title: ChartSeries.marker property
linktitle: marker property
articleTitle: marker property
second_title: Aspose.Words for Python
description: "ChartSeries.marker property. Specifies a data marker"
type: docs
weight: 100
url: /python-net/aspose.words.drawing.charts/chartseries/marker/
---

## ChartSeries.marker property

Specifies a data marker. Marker is automatically created when requested.


```python
@property
def marker(self) -> aspose.words.drawing.charts.ChartMarker:
    ...

```

### Examples

Show how to set marker formatting.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.SCATTER, width=432, height=252)
chart = shape.chart
# Delete default generated series.
chart.series.clear()
series = chart.series.add_double(series_name='AW Series 1', x_values=[0.7, 1.8, 2.6, 3.9], y_values=[2.7, 3.2, 0.8, 1.7])
# Set marker formatting.
series.marker.size = 40
series.marker.symbol = aw.drawing.charts.MarkerSymbol.SQUARE
data_points = series.data_points
data_points[0].marker.format.fill.preset_textured(aw.drawing.PresetTexture.DENIM)
data_points[0].marker.format.stroke.fore_color = aspose.pydrawing.Color.yellow
data_points[0].marker.format.stroke.back_color = aspose.pydrawing.Color.red
data_points[1].marker.format.fill.preset_textured(aw.drawing.PresetTexture.WATER_DROPLETS)
data_points[1].marker.format.stroke.fore_color = aspose.pydrawing.Color.yellow
data_points[1].marker.format.stroke.visible = False
data_points[2].marker.format.fill.preset_textured(aw.drawing.PresetTexture.GREEN_MARBLE)
data_points[2].marker.format.stroke.fore_color = aspose.pydrawing.Color.yellow
data_points[3].marker.format.fill.preset_textured(aw.drawing.PresetTexture.OAK)
data_points[3].marker.format.stroke.fore_color = aspose.pydrawing.Color.yellow
data_points[3].marker.format.stroke.transparency = 0.5
doc.save(file_name=ARTIFACTS_DIR + 'Charts.MarkerFormatting.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartSeries](../)

