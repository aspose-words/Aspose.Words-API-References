---
title: PresetTexture enumeration
linktitle: PresetTexture enumeration
articleTitle: PresetTexture enumeration
second_title: Aspose.Words for Python
description: "aspose.words.drawing.PresetTexture enumeration. Specifies texture to be used to fill a shape."
type: docs
weight: 280
url: /python-net/aspose.words.drawing/presettexture/
---

## PresetTexture enumeration

Specifies texture to be used to fill a shape.


### Members

| Name | Description |
| --- | --- |
| NONE | No Texture. |
| BLUE_TISSUE_PAPER | Blue tissue paper texture. |
| BOUQUET | Bouquet texture. |
| BROWN_MARBLE | Brown marble texture. |
| CANVAS | Canvas texture. |
| CORK | Cork texture. |
| DENIM | Denim texture. |
| FISH_FOSSIL | Fish fossil texture. |
| GRANITE | Granite texture. |
| GREEN_MARBLE | Green marble texture. |
| MEDIUM_WOOD | Medium wood texture. |
| NEWSPRINT | Newsprint texture. |
| OAK | Oak texture. |
| PAPER_BAG | Paper bag texture. |
| PAPYRUS | Papyrus texture. |
| PARCHMENT | Parchment texture. |
| PINK_TISSUE_PAPER | Pink tissue paper texture. |
| PURPLE_MESH | Purple mesh texture. |
| RECYCLED_PAPER | Recycled paper texture. |
| SAND | Sand texture. |
| STATIONERY | Stationery texture. |
| WALNUT | Walnut texture. |
| WATER_DROPLETS | Water droplets texture. |
| WHITE_MARBLE | White marble texture. |
| WOVEN_MAT | Woven mat texture. |

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

* module [aspose.words.drawing](../)

