---
title: Fill.preset_textured method
linktitle: preset_textured method
articleTitle: preset_textured method
second_title: Aspose.Words for Python
description: "Fill.preset_textured method. Sets the fill to a preset texture."
type: docs
weight: 240
url: /python-net/aspose.words.drawing/fill/preset_textured/
---

## preset_textured(preset_texture) {#presettexture}

Sets the fill to a preset texture.


```python
def preset_textured(self, preset_texture: aspose.words.drawing.PresetTexture):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| preset_texture | [PresetTexture](../../presettexture/) |  |

### Examples

Show how to set marker formatting.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

shape = builder.insert_chart(aw.drawing.charts.ChartType.SCATTER, 432, 252)
chart = shape.chart

# Delete default generated series.
chart.series.clear()
series = chart.series.add("AW Series 1", x_values=[0.7, 1.8, 2.6, 3.9], y_values=[2.7, 3.2, 0.8, 1.7])

# Set marker formatting.
series.marker.size = 40
series.marker.symbol = aw.drawing.charts.MarkerSymbol.SQUARE
data_points = series.data_points
data_points[0].marker.format.fill.preset_textured(aw.drawing.PresetTexture.DENIM)
data_points[0].marker.format.stroke.fore_color = drawing.Color.yellow
data_points[0].marker.format.stroke.back_color = drawing.Color.red
data_points[1].marker.format.fill.preset_textured(aw.drawing.PresetTexture.WATER_DROPLETS)
data_points[1].marker.format.stroke.fore_color = drawing.Color.yellow
data_points[1].marker.format.stroke.visible = False
data_points[2].marker.format.fill.preset_textured(aw.drawing.PresetTexture.GREEN_MARBLE)
data_points[2].marker.format.stroke.fore_color = drawing.Color.yellow
data_points[3].marker.format.fill.preset_textured(aw.drawing.PresetTexture.OAK)
data_points[3].marker.format.stroke.fore_color = drawing.Color.yellow
data_points[3].marker.format.stroke.transparency = 0.5

doc.save(ARTIFACTS_DIR + "Charts.marker_formatting.docx")
```

### See Also

* module [aspose.words.drawing](../../)
* class [Fill](../)

