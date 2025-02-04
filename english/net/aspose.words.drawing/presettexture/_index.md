---
title: PresetTexture Enum
linktitle: PresetTexture
articleTitle: PresetTexture
second_title: Aspose.Words for .NET
description: Aspose.Words.Drawing.PresetTexture enum. Specifies texture to be used to fill a shape in C#.
type: docs
weight: 1550
url: /net/aspose.words.drawing/presettexture/
---
## PresetTexture enumeration

Specifies texture to be used to fill a shape.

```csharp
public enum PresetTexture
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| None | `-1` | No Texture. |
| BlueTissuePaper | `1` | Blue tissue paper texture. |
| Bouquet | `2` | Bouquet texture. |
| BrownMarble | `3` | Brown marble texture. |
| Canvas | `4` | Canvas texture. |
| Cork | `5` | Cork texture. |
| Denim | `6` | Denim texture. |
| FishFossil | `7` | Fish fossil texture. |
| Granite | `8` | Granite texture. |
| GreenMarble | `9` | Green marble texture. |
| MediumWood | `10` | Medium wood texture. |
| Newsprint | `11` | Newsprint texture. |
| Oak | `12` | Oak texture. |
| PaperBag | `13` | Paper bag texture. |
| Papyrus | `14` | Papyrus texture. |
| Parchment | `15` | Parchment texture. |
| PinkTissuePaper | `16` | Pink tissue paper texture. |
| PurpleMesh | `17` | Purple mesh texture. |
| RecycledPaper | `18` | Recycled paper texture. |
| Sand | `19` | Sand texture. |
| Stationery | `20` | Stationery texture. |
| Walnut | `21` | Walnut texture. |
| WaterDroplets | `22` | Water droplets texture. |
| WhiteMarble | `23` | White marble texture. |
| WovenMat | `24` | Woven mat texture. |

## Examples

Show how to set marker formatting.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Scatter, 432, 252);
Chart chart = shape.Chart;

// Delete default generated series.
chart.Series.Clear();
ChartSeries series = chart.Series.Add("AW Series 1", new[] { 0.7, 1.8, 2.6, 3.9 },
    new[] { 2.7, 3.2, 0.8, 1.7 });

// Set marker formatting.
series.Marker.Size = 40;
series.Marker.Symbol = MarkerSymbol.Square;
ChartDataPointCollection dataPoints = series.DataPoints;
dataPoints[0].Marker.Format.Fill.PresetTextured(PresetTexture.Denim);
dataPoints[0].Marker.Format.Stroke.ForeColor = Color.Yellow;
dataPoints[0].Marker.Format.Stroke.BackColor = Color.Red;
dataPoints[1].Marker.Format.Fill.PresetTextured(PresetTexture.WaterDroplets);
dataPoints[1].Marker.Format.Stroke.ForeColor = Color.Yellow;
dataPoints[1].Marker.Format.Stroke.Visible = false;
dataPoints[2].Marker.Format.Fill.PresetTextured(PresetTexture.GreenMarble);
dataPoints[2].Marker.Format.Stroke.ForeColor = Color.Yellow;
dataPoints[3].Marker.Format.Fill.PresetTextured(PresetTexture.Oak);
dataPoints[3].Marker.Format.Stroke.ForeColor = Color.Yellow;
dataPoints[3].Marker.Format.Stroke.Transparency = 0.5;

doc.Save(ArtifactsDir + "Charts.MarkerFormatting.docx");
```

### See Also

* namespace [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assembly [Aspose.Words](../../)
