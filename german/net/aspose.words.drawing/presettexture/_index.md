---
title: PresetTexture Enum
linktitle: PresetTexture
articleTitle: PresetTexture
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aufzählung Aspose.Words.Drawing.PresetTexture, um Ihre Formen mit anpassbaren Texturen für beeindruckende Dokumentdesigns zu verbessern.
type: docs
weight: 1560
url: /de/net/aspose.words.drawing/presettexture/
---
## PresetTexture enumeration

Gibt die Textur an, die zum Füllen einer Form verwendet werden soll.

```csharp
public enum PresetTexture
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| None | `-1` | Keine Textur. |
| BlueTissuePaper | `1` | Blaue Seidenpapierstruktur. |
| Bouquet | `2` | Blumenstraußtextur. |
| BrownMarble | `3` | Braune Marmorstruktur. |
| Canvas | `4` | Leinwandstruktur. |
| Cork | `5` | Korkstruktur. |
| Denim | `6` | Denim-Textur. |
| FishFossil | `7` | Textur eines Fischfossils. |
| Granite | `8` | Granitstruktur. |
| GreenMarble | `9` | Grüne Marmorstruktur. |
| MediumWood | `10` | Mittlere Holzstruktur. |
| Newsprint | `11` | Zeitungspapierstruktur. |
| Oak | `12` | Eichenstruktur. |
| PaperBag | `13` | Papiertütenstruktur. |
| Papyrus | `14` | Papyrustextur. |
| Parchment | `15` | Pergamentstruktur. |
| PinkTissuePaper | `16` | Rosa Seidenpapierstruktur. |
| PurpleMesh | `17` | Lila Netztextur. |
| RecycledPaper | `18` | Textur aus Recyclingpapier. |
| Sand | `19` | Sandtextur. |
| Stationery | `20` | Briefpapiertextur. |
| Walnut | `21` | Walnussstruktur. |
| WaterDroplets | `22` | Wassertropfen-Textur. |
| WhiteMarble | `23` | Weiße Marmorstruktur. |
| WovenMat | `24` | Gewebte Mattenstruktur. |

## Beispiele

Zeigen Sie, wie Sie die Markierungsformatierung festlegen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Scatter, 432, 252);
Chart chart = shape.Chart;

// Standardmäßig generierte Serien löschen.
chart.Series.Clear();
ChartSeries series = chart.Series.Add("AW Series 1", new[] { 0.7, 1.8, 2.6, 3.9 },
    new[] { 2.7, 3.2, 0.8, 1.7 });

// Markierungsformatierung festlegen.
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

### Siehe auch

* namensraum [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Montage [Aspose.Words](../../)
