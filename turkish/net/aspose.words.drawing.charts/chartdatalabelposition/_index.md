---
title: ChartDataLabelPosition Enum
linktitle: ChartDataLabelPosition
articleTitle: ChartDataLabelPosition
second_title: .NET için Aspose.Words
description: Grafik veri etiketlerinizi daha iyi anlaşılırlık ve sunum için kolayca özelleştirmek amacıyla Aspose.Words.ChartDataLabelPosition enum'unu keşfedin.
type: docs
weight: 960
url: /tr/net/aspose.words.drawing.charts/chartdatalabelposition/
---
## ChartDataLabelPosition enumeration

Bir grafik veri etiketi için konumu belirtir.

```csharp
public enum ChartDataLabelPosition
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Center | `0` | Bir veri etiketinin bir veri işaretçisinin ortasında görüntülenmesi gerektiğini belirtir. |
| Left | `1` | Bir veri etiketinin bir veri işaretçisinin solunda görüntülenmesi gerektiğini belirtir. |
| Right | `2` | Bir veri etiketinin bir veri işaretçisinin sağında görüntülenmesi gerektiğini belirtir. |
| Above | `3` | Bir veri etiketinin bir veri işaretçisinin üstünde görüntülenmesi gerektiğini belirtir. |
| Below | `4` | Bir veri etiketinin bir veri işaretçisinin altında görüntülenmesi gerektiğini belirtir. |
| InsideBase | `5` | Bir veri etiketinin bir veri işaretçisinin tabanının içinde görüntülenmesi gerektiğini belirtir. |
| InsideEnd | `6` | Bir veri etiketinin bir veri işaretçisinin sonunda görüntülenmesi gerektiğini belirtir. |
| OutsideEnd | `7` | Bir veri etiketinin bir veri işaretçisinin sonunun dışında görüntülenmesi gerektiğini belirtir. |
| BestFit | `8` | Bir veri etiketinin en uygun konumda görüntülenmesi gerektiğini belirtir. |

## Notlar

Tüm seri türleri etiket konumlarını belirtmenize izin vermez. Ve izin verenler tüm değerleri desteklemez.

## Örnekler

Veri etiketinin konumunun nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Sütun grafiği ekle.
Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeriesCollection seriesColl = chart.Series;

// Varsayılan olarak oluşturulan seriyi sil.
seriesColl.Clear();

// Seri ekle.
ChartSeries series = seriesColl.Add(
    "Series 1",
    new string[] { "Category 1", "Category 2", "Category 3" },
    new double[] { 4, 5, 6 });

// Veri etiketlerini göster ve yazı tipi rengini ayarla.
series.HasDataLabels = true;
ChartDataLabelCollection dataLabels = series.DataLabels;
dataLabels.ShowValue = true;
dataLabels.Font.Color = Color.White;

// Veri etiketi konumunu ayarla.
dataLabels.Position = ChartDataLabelPosition.InsideBase;
dataLabels[0].Position = ChartDataLabelPosition.OutsideEnd;
dataLabels[0].Font.Color = Color.DarkRed;

doc.Save(ArtifactsDir + "Charts.LabelPosition.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../)
