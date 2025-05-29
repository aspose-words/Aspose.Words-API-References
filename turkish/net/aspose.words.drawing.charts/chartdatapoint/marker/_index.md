---
title: ChartDataPoint.Marker
linktitle: Marker
articleTitle: Marker
second_title: .NET için Aspose.Words
description: Daha net içgörüler ve etkili görselleştirmeler için grafiklerinizi özelleştirilebilir veri işaretleyicileriyle geliştirmek üzere ChartDataPoint Marker özelliğini keşfedin.
type: docs
weight: 60
url: /tr/net/aspose.words.drawing.charts/chartdatapoint/marker/
---
## ChartDataPoint.Marker property

Grafik veri işaretçisini belirtir.

```csharp
public ChartMarker Marker { get; }
```

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

* class [ChartMarker](../../chartmarker/)
* class [ChartDataPoint](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)
