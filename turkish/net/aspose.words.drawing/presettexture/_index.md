---
title: PresetTexture Enum
linktitle: PresetTexture
articleTitle: PresetTexture
second_title: .NET için Aspose.Words
description: Çarpıcı belge tasarımları için şekillerinizi özelleştirilebilir dokularla geliştirmek üzere Aspose.Words.Drawing.PresetTexture enumunu keşfedin.
type: docs
weight: 1560
url: /tr/net/aspose.words.drawing/presettexture/
---
## PresetTexture enumeration

Bir şekli doldurmak için kullanılacak dokuyu belirtir.

```csharp
public enum PresetTexture
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| None | `-1` | Doku Yok. |
| BlueTissuePaper | `1` | Mavi kağıt mendil dokusu. |
| Bouquet | `2` | Buket dokusu. |
| BrownMarble | `3` | Kahverengi mermer dokusu. |
| Canvas | `4` | Tuval dokusu. |
| Cork | `5` | Mantar dokusu. |
| Denim | `6` | Kot dokusu. |
| FishFossil | `7` | Balık fosili dokusu. |
| Granite | `8` | Granit dokusu. |
| GreenMarble | `9` | Yeşil mermer dokusu. |
| MediumWood | `10` | Orta ahşap dokusu. |
| Newsprint | `11` | Gazete kağıdı dokusu. |
| Oak | `12` | Meşe dokusu. |
| PaperBag | `13` | Kağıt torba dokusu. |
| Papyrus | `14` | Papirüs dokusu. |
| Parchment | `15` | Parşömen dokusu. |
| PinkTissuePaper | `16` | Pembe kağıt mendil dokusu. |
| PurpleMesh | `17` | Mor örgü dokusu. |
| RecycledPaper | `18` | Geri dönüştürülmüş kağıt dokusu. |
| Sand | `19` | Kum dokusu. |
| Stationery | `20` | Kırtasiye dokusu. |
| Walnut | `21` | Ceviz dokusu. |
| WaterDroplets | `22` | Su damlacıkları dokusu. |
| WhiteMarble | `23` | Beyaz mermer dokusu. |
| WovenMat | `24` | Dokuma paspas dokusu. |

## Örnekler

İşaretçi biçimlendirmesinin nasıl ayarlanacağını göster.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Scatter, 432, 252);
Chart chart = shape.Chart;

// Varsayılan olarak oluşturulan seriyi sil.
chart.Series.Clear();
ChartSeries series = chart.Series.Add("AW Series 1", new[] { 0.7, 1.8, 2.6, 3.9 },
    new[] { 2.7, 3.2, 0.8, 1.7 });

// İşaretçi biçimlendirmesini ayarlayın.
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

### Ayrıca bakınız

* ad alanı [Aspose.Words.Drawing](../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../)
