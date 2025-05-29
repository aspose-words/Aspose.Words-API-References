---
title: PresetTexture Enum
linktitle: PresetTexture
articleTitle: PresetTexture
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.Drawing.PresetTexture-uppräkningen för att förbättra dina former med anpassningsbara texturer för fantastiska dokumentdesigner.
type: docs
weight: 1560
url: /sv/net/aspose.words.drawing/presettexture/
---
## PresetTexture enumeration

Anger textur som ska användas för att fylla en form.

```csharp
public enum PresetTexture
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| None | `-1` | Ingen textur. |
| BlueTissuePaper | `1` | Blå silkespappersstruktur. |
| Bouquet | `2` | Bukettstruktur. |
| BrownMarble | `3` | Brun marmorstruktur. |
| Canvas | `4` | Canvasstruktur. |
| Cork | `5` | Korkstruktur. |
| Denim | `6` | Denimstruktur. |
| FishFossil | `7` | Fiskfossilstruktur. |
| Granite | `8` | Granitstruktur. |
| GreenMarble | `9` | Grön marmorstruktur. |
| MediumWood | `10` | Medelstor trästruktur. |
| Newsprint | `11` | Tidningspappersstruktur. |
| Oak | `12` | Ekstruktur. |
| PaperBag | `13` | Papperspåsestruktur. |
| Papyrus | `14` | Papyrusstruktur. |
| Parchment | `15` | Pergamentstruktur. |
| PinkTissuePaper | `16` | Rosa silkespappersstruktur. |
| PurpleMesh | `17` | Lila nätstruktur. |
| RecycledPaper | `18` | Återvunnet pappersstruktur. |
| Sand | `19` | Sandstruktur. |
| Stationery | `20` | Kontorsmaterial. |
| Walnut | `21` | Valnötsstruktur. |
| WaterDroplets | `22` | Vattendroppar textur. |
| WhiteMarble | `23` | Vit marmorstruktur. |
| WovenMat | `24` | Vävd mattstruktur. |

## Exempel

Visa hur man ställer in markörformatering.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Scatter, 432, 252);
Chart chart = shape.Chart;

// Radera standardgenererad serie.
chart.Series.Clear();
ChartSeries series = chart.Series.Add("AW Series 1", new[] { 0.7, 1.8, 2.6, 3.9 },
    new[] { 2.7, 3.2, 0.8, 1.7 });

// Ange markörformatering.
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

### Se även

* namnutrymme [Aspose.Words.Drawing](../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../)
