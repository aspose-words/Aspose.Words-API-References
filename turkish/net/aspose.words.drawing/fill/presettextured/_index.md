---
title: Fill.PresetTextured
linktitle: PresetTextured
articleTitle: PresetTextured
second_title: .NET için Aspose.Words
description: Çarpıcı önceden ayarlanmış dokuları zahmetsizce uygulamak ve tasarımlarınızı benzersiz görsel çekicilikle geliştirmek için Fill PresetTextured yöntemini keşfedin.
type: docs
weight: 240
url: /tr/net/aspose.words.drawing/fill/presettextured/
---
## Fill.PresetTextured method

Dolguyu önceden ayarlanmış bir dokuya ayarlar.

```csharp
public void PresetTextured(PresetTexture presetTexture)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| presetTexture | PresetTexture | [`PresetTexture`](../../presettexture/) |

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

* enum [PresetTexture](../../presettexture/)
* class [Fill](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
